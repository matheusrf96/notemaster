var app = new Vue({
    el: '#app',
    data: {
        title: "Notemaster",
        note: {
            title: '',
            content: ''
        },
        notes: [
            {
                title: "Test 01",
                content: "Primeiro Text",
                date: new Date(Date.now()).toLocaleString()
            }
        ]
    },
    methods: {
        addNote(){
            let {title, content} = this.note

            this.notes.push({
                title,
                content,
                date: new Date(Date.now()).toLocaleString()
            })
        },
        removeNote(index){
            this.notes.splice(index, 1)
        }
    }
})