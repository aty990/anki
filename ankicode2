<script>
function incrementalReveal() {
    let remaining = Array.prototype.slice.call(
        document.getElementsByClassName("cloze"))
    let content = []
    for (let cloze of remaining) {
        content.push(cloze.innerHTML)
        cloze.innerHTML = "[...]"
    }
    remaining[0].classList.add("active")

    document.addEventListener("keydown", (event) => {
        // https://keycode.info/
        if (event.keyCode == 72) {
            revealNext()			
        } else if (event.keyCode == 71) revealAll()
    })
    let revealAll = () => {
        while (remaining) {
            let cloze = remaining.shift()
            cloze.innerHTML = content.shift()
            cloze.classList.remove("active")
        }
    }
    let revealNext = () => {
        let cloze = remaining.shift()
        cloze.innerHTML = content.shift()
        cloze.classList.remove("active")
        remaining[0].classList.add("active")
    }
}
incrementalReveal()
</script>
