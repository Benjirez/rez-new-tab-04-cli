<script>
import {myData, selectedOption} from './myDataStore.js'

    const doDelete = async ()=>{
    
        const res = await fetch('https://rez-new-tab-04.onrender.com/old/' + $selectedOption._id, {
            method: "DELETE"
        })
    
        //const newUsers = await res.json()
        //console.log( res.json() )
        $myData = await res.json()
    
    }
    </script>
    
    <button on:click={doDelete}>delete</button>