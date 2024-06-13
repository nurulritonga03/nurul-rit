$(document).ready(function() {
    // Toggle form visibility
    $('#toggle-form').click(function() {
        $('#form-container').slideToggle();
    });

    // Add book to the list
    $('#book-form').submit(function(event) {
        event.preventDefault();
        const title = $('#title').val();
        const author = $('#author').val();
        
        if (title && author) {
            $('#book-list').append(`<div class="book"><h3>${title}</h3><p>${author}</p><button class="remove-book">Hapus</button></div>`);
            $('#title').val('');
            $('#author').val('');
            $('#form-container').slideUp();
        } else {
            alert('Silakan isi semua field!');
        }
    });

    // Remove book from the list
    $('#book-list').on('click', '.remove-book', function() {
        $(this).parent().animate({
            opacity: 0,
            height: 'toggle'
        }, 600, function() {
            $(this).remove();
        });
    });
});
