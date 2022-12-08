<script>
export default {
    mounted() {
        window.addEventListener('scroll', () => {
            const windowBottom = window.innerHeight + window.scrollY;
            const windowTop = window.scrollY;
            
            for(const image of this.images) {
                const imageHalfPoint = image.offsetTop + image.offsetHeight / 2;
                const imageBottom = image.offsetTop + image.offsetHeight;
                const imageTop = image.offsetTop;

                if(windowTop > imageBottom || windowBottom < imageTop) {
                    if(image.classList.contains('float-left')) image.classList.add('hidden-left');
                    else image.classList.add('hidden-right');
                } else if(windowBottom > imageHalfPoint) {
                    if(image.classList.contains('float-left')) image.classList.remove('hidden-left');
                    else image.classList.remove('hidden-right');
                }
            }
            
        });
    },
    computed: {
        images() {
            return [this.$refs.img1, this.$refs.img2, this.$refs.img3];
        }
    }
}
</script>

<template>
    <div class="container">
        <h1>Slide in on Scroll</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Odio dolore reiciendis corrupti quae quo? Perspiciatis totam illum quam doloribus nisi, maxime nemo, eligendi illo, id iste explicabo repellendus harum optio rem iusto sit! Nulla, nesciunt, odio rerum doloremque nostrum sint tempore repellat dolore facilis ab, minus ullam excepturi? Sequi, dolor reiciendis mollitia veritatis distinctio veniam neque, quisquam provident nobis enim vel corporis culpa eius repellendus! Nemo fugit neque distinctio debitis voluptate nostrum minus earum eius dicta. Labore animi iste nam quasi id, perferendis doloremque voluptatem quo sapiente aperiam natus perspiciatis doloribus voluptas dolorem qui possimus sunt rerum sit soluta ab.</p>
        <br>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit impedit dicta voluptatibus animi, in ullam, fuga distinctio soluta ipsam error, nobis eveniet expedita quo repudiandae hic eaque assumenda unde vitae earum minima. Odit reiciendis voluptatibus magnam quas saepe, nisi non eveniet, consequatur veritatis necessitatibus deleniti libero, magni temporibus! Molestias alias inventore aliquid minima impedit eaque a, dolor sit consequuntur eos deleniti repellendus, corrupti dolore natus id! Earum, quae dolores atque quo asperiores molestiae neque doloribus delectus qui officia veritatis vero aliquid accusantium tempore facilis voluptate pariatur dicta labore sit. Numquam, est, provident aspernatur quo aliquam corporis mollitia non cupiditate perspiciatis officia pariatur placeat quia iure sapiente voluptates sequi, amet autem deserunt soluta eum nostrum odio! Optio, corrupti enim dolorem, cupiditate laudantium fugit neque minus, dolores voluptate quas dignissimos recusandae quia dolore rerum vero veniam eius quasi assumenda. Iure quam officia similique dicta pariatur fugiat. Repudiandae voluptatibus veniam illo facilis doloremque, voluptate optio nostrum minus repellendus cupiditate quos cum minima, pariatur iure natus. Assumenda possimus facilis cupiditate quisquam, quia pariatur ex rem aut a natus rerum amet explicabo dolor beatae id asperiores! Dolorum illum quo at mollitia quia doloremque, repellat quam sint culpa labore deserunt deleniti optio consequatur! Architecto, corporis magnam.</p>
        <br>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. A, quam, dolores tempore sunt dolore vitae aut laborum quia, tenetur illum corrupti rerum quod eaque blanditiis nobis hic dolorem nulla repellat nam. Placeat perferendis eius possimus consequuntur. Aliquid culpa, esse ea, perspiciatis dolor expedita nisi tempora similique dolorum perferendis laborum, soluta in magni harum alias quam eum impedit sed illum dolore illo tenetur? Soluta quibusdam in itaque qui quos ipsam. Quae quam consequatur similique fugit nam dolores iste tenetur natus ullam beatae dignissimos, eius, ipsa eligendi, harum reiciendis dolorum qui. Assumenda nostrum, magni temporibus odit autem optio eius nihil doloribus fuga ullam similique molestias sint voluptatibus nemo illum recusandae facilis provident unde? Possimus ea tenetur veritatis esse. Magni totam reprehenderit vero?</p>
        <br>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam distinctio culpa quos impedit expedita nam laudantium, excepturi odio, debitis veritatis incidunt minus itaque ex quisquam aliquid harum atque nesciunt error quidem? Perspiciatis repellat asperiores cum repellendus? Sapiente quia quam sint consequatur nisi, culpa, esse, nulla blanditiis iusto voluptate deleniti amet. Nulla ut necessitatibus repellendus obcaecati sapiente. Beatae facere sapiente, tenetur iste aperiam similique, odio, fugiat ducimus itaque suscipit nemo consequatur laboriosam neque corrupti. Temporibus cum quae, laudantium neque iure magni autem unde officia sequi quas ducimus animi blanditiis ut tempore qui, ab cupiditate, voluptate facilis rerum. Voluptas consequuntur dolore, iste dolor ratione sint rem impedit sequi eligendi. Vitae, est. Sint assumenda quae aliquam in asperiores dolore exercitationem tempora eos perferendis eaque, error cupiditate ducimus temporibus fugiat laudantium quos atque reprehenderit delectus ipsa saepe inventore? Unde beatae, aliquid labore repellat inventore est adipisci dolorum qui. Voluptates eligendi dolorum nam quaerat.</p>
        <br>

        <div ref="img1" class="img-container float-left hidden-left">
            <img src="./assets/img1-400x400.jpg" alt="picture of a field">
        </div>

        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit impedit dicta voluptatibus animi, in ullam, fuga distinctio soluta ipsam error, nobis eveniet expedita quo repudiandae hic eaque assumenda unde vitae earum minima. Odit reiciendis voluptatibus magnam quas saepe, nisi non eveniet, consequatur veritatis necessitatibus deleniti libero, magni temporibus! Molestias alias inventore aliquid minima impedit eaque a, dolor sit consequuntur eos deleniti repellendus, corrupti dolore natus id! Earum, quae dolores atque quo asperiores molestiae neque doloribus delectus qui officia veritatis vero aliquid accusantium tempore facilis voluptate pariatur dicta labore sit. Numquam, est, provident aspernatur quo aliquam corporis mollitia non cupiditate perspiciatis officia pariatur placeat quia iure sapiente voluptates sequi, amet autem deserunt soluta eum nostrum odio! Optio, corrupti enim dolorem, cupiditate laudantium fugit neque minus, dolores voluptate quas dignissimos recusandae quia dolore rerum vero veniam eius quasi assumenda. Iure quam officia similique dicta pariatur fugiat. Repudiandae voluptatibus veniam illo facilis doloremque, voluptate optio nostrum minus repellendus cupiditate quos cum minima, pariatur iure natus. Assumenda possimus facilis cupiditate quisquam, quia pariatur ex rem aut a natus rerum amet explicabo dolor beatae id asperiores! Dolorum illum quo at mollitia quia doloremque, repellat quam sint culpa labore deserunt deleniti optio consequatur! Architecto, corporis magnam.</p>
        <br>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem qui hic, aspernatur possimus eaque velit cupiditate ex minus praesentium sit vero in ducimus quod delectus sed reiciendis nesciunt. Rem ab temporibus quasi doloremque impedit quam est ipsa necessitatibus vel, officiis explicabo fugit quibusdam aspernatur inventore, deserunt consectetur labore eveniet commodi recusandae expedita similique quae modi. Expedita debitis similique beatae earum delectus suscipit, commodi repellat perspiciatis quod esse tempore est iusto ipsam repellendus tenetur vero. Eum nihil repellat quibusdam iusto autem earum aliquam iure quia, dolorem consequuntur id, impedit maiores molestiae ipsam? Harum quasi officiis, non repudiandae nesciunt vero ipsa ab?</p>
        <br>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic laboriosam distinctio culpa quos impedit expedita nam laudantium, excepturi odio, debitis veritatis incidunt minus itaque ex quisquam aliquid harum atque nesciunt error quidem? Perspiciatis repellat asperiores cum repellendus? Sapiente quia quam sint consequatur nisi, culpa, esse, nulla blanditiis iusto voluptate deleniti amet. Nulla ut necessitatibus repellendus obcaecati sapiente. Beatae facere sapiente, tenetur iste aperiam similique, odio, fugiat ducimus itaque suscipit nemo consequatur laboriosam neque corrupti. Temporibus cum quae, laudantium neque iure magni autem unde officia sequi quas ducimus animi blanditiis ut tempore qui, ab cupiditate, voluptate facilis rerum. Voluptas consequuntur dolore, iste dolor ratione sint rem impedit sequi eligendi. Vitae, est. Sint assumenda quae aliquam in asperiores dolore exercitationem tempora eos perferendis eaque, error cupiditate ducimus temporibus fugiat laudantium quos atque reprehenderit delectus ipsa saepe inventore? Unde beatae, aliquid labore repellat inventore est adipisci dolorum qui. Voluptates eligendi dolorum nam quaerat.</p>
        <br>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias eum aut deserunt, beatae error in quibusdam est blanditiis ipsum distinctio dolorem dolores facere commodi incidunt sequi illo maiores id quidem temporibus? Tempore eveniet beatae molestiae rerum voluptas aliquam, inventore iusto, veniam itaque iste delectus? Debitis aliquam esse consequuntur corporis, provident optio quasi illo ullam vel nulla ut distinctio alias ducimus, laborum in minus repellat consequatur ad dignissimos quis ratione. Consectetur amet quae modi repellendus magnam, magni commodi cumque quaerat culpa, possimus quibusdam nihil vel? Perferendis adipisci ducimus repudiandae iste a libero officia, odio rerum, pariatur ullam eaque quae distinctio eligendi, velit tenetur voluptas? Sunt, harum excepturi provident eum obcaecati modi quasi a tempore deleniti recusandae amet ex, labore consectetur est quidem neque iste dolore aut, culpa laborum. Et ipsum doloribus, placeat exercitationem suscipit quisquam reprehenderit cupiditate tempora culpa iure ullam dolores, autem inventore corrupti blanditiis? Aut dolorem aspernatur asperiores hic! Quibusdam, quas at iusto earum necessitatibus nemo voluptatum numquam totam vero optio consequatur, sed cupiditate natus quisquam enim reprehenderit odit quasi laboriosam sint exercitationem nulla officia ea nesciunt dolor. Deserunt cum excepturi explicabo amet perspiciatis alias corporis ratione veritatis nobis sapiente deleniti, ex voluptates, ipsum temporibus magnam voluptatum aspernatur harum.</p>
        <br>

        <div ref="img2" class="img-container float-right hidden-right">
            <img src="./assets/img2-400x401.jpg" alt="picture of a tower">
        </div>

        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit impedit dicta voluptatibus animi, in ullam, fuga distinctio soluta ipsam error, nobis eveniet expedita quo repudiandae hic eaque assumenda unde vitae earum minima. Odit reiciendis voluptatibus magnam quas saepe, nisi non eveniet, consequatur veritatis necessitatibus deleniti libero, magni temporibus! Molestias alias inventore aliquid minima impedit eaque a, dolor sit consequuntur eos deleniti repellendus, corrupti dolore natus id! Earum, quae dolores atque quo asperiores molestiae neque doloribus delectus qui officia veritatis vero aliquid accusantium tempore facilis voluptate pariatur dicta labore sit. Numquam, est, provident aspernatur quo aliquam corporis mollitia non cupiditate perspiciatis officia pariatur placeat quia iure sapiente voluptates sequi, amet autem deserunt soluta eum nostrum odio! Optio, corrupti enim dolorem, cupiditate laudantium fugit neque minus, dolores voluptate quas dignissimos recusandae quia dolore rerum vero veniam eius quasi assumenda. Iure quam officia similique dicta pariatur fugiat. Repudiandae voluptatibus veniam illo facilis doloremque, voluptate optio nostrum minus repellendus cupiditate quos cum minima, pariatur iure natus. Assumenda possimus facilis cupiditate quisquam, quia pariatur ex rem aut a natus rerum amet explicabo dolor beatae id asperiores! Dolorum illum quo at mollitia quia doloremque, repellat quam sint culpa labore deserunt deleniti optio consequatur! Architecto, corporis magnam.</p>
        <br>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem qui hic, aspernatur possimus eaque velit cupiditate ex minus praesentium sit vero in ducimus quod delectus sed reiciendis nesciunt. Rem ab temporibus quasi doloremque impedit quam est ipsa necessitatibus vel, officiis explicabo fugit quibusdam aspernatur inventore, deserunt consectetur labore eveniet commodi recusandae expedita similique quae modi. Expedita debitis similique beatae earum delectus suscipit, commodi repellat perspiciatis quod esse tempore est iusto ipsam repellendus tenetur vero. Eum nihil repellat quibusdam iusto autem earum aliquam iure quia, dolorem consequuntur id, impedit maiores molestiae ipsam? Harum quasi officiis, non repudiandae nesciunt vero ipsa ab?</p>
        <br>

        <div ref="img3" class="img-container float-left hidden-left">
            <img src="./assets/img3-400x400.jpg" alt="picture of a camera">
        </div>

        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit impedit dicta voluptatibus animi, in ullam, fuga distinctio soluta ipsam error, nobis eveniet expedita quo repudiandae hic eaque assumenda unde vitae earum minima. Odit reiciendis voluptatibus magnam quas saepe, nisi non eveniet, consequatur veritatis necessitatibus deleniti libero, magni temporibus! Molestias alias inventore aliquid minima impedit eaque a, dolor sit consequuntur eos deleniti repellendus, corrupti dolore natus id! Earum, quae dolores atque quo asperiores molestiae neque doloribus delectus qui officia veritatis vero aliquid accusantium tempore facilis voluptate pariatur dicta labore sit. Numquam, est, provident aspernatur quo aliquam corporis mollitia non cupiditate perspiciatis officia pariatur placeat quia iure sapiente voluptates sequi, amet autem deserunt soluta eum nostrum odio! Optio, corrupti enim dolorem, cupiditate laudantium fugit neque minus, dolores voluptate quas dignissimos recusandae quia dolore rerum vero veniam eius quasi assumenda. Iure quam officia similique dicta pariatur fugiat. Repudiandae voluptatibus veniam illo facilis doloremque, voluptate optio nostrum minus repellendus cupiditate quos cum minima, pariatur iure natus. Assumenda possimus facilis cupiditate quisquam, quia pariatur ex rem aut a natus rerum amet explicabo dolor beatae id asperiores! Dolorum illum quo at mollitia quia doloremque, repellat quam sint culpa labore deserunt deleniti optio consequatur! Architecto, corporis magnam.</p>
        <br>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Molestias eum aut deserunt, beatae error in quibusdam est blanditiis ipsum distinctio dolorem dolores facere commodi incidunt sequi illo maiores id quidem temporibus? Tempore eveniet beatae molestiae rerum voluptas aliquam, inventore iusto, veniam itaque iste delectus? Debitis aliquam esse consequuntur corporis, provident optio quasi illo ullam vel nulla ut distinctio alias ducimus, laborum in minus repellat consequatur ad dignissimos quis ratione. Consectetur amet quae modi repellendus magnam, magni commodi cumque quaerat culpa, possimus quibusdam nihil vel? Perferendis adipisci ducimus repudiandae iste a libero officia, odio rerum, pariatur ullam eaque quae distinctio eligendi, velit tenetur voluptas? Sunt, harum excepturi provident eum obcaecati modi quasi a tempore deleniti recusandae amet ex, labore consectetur est quidem neque iste dolore aut, culpa laborum. Et ipsum doloribus, placeat exercitationem suscipit quisquam reprehenderit cupiditate tempora culpa iure ullam dolores, autem inventore corrupti blanditiis? Aut dolorem aspernatur asperiores hic! Quibusdam, quas at iusto earum necessitatibus nemo voluptatum numquam totam vero optio consequatur, sed cupiditate natus quisquam enim reprehenderit odit quasi laboriosam sint exercitationem nulla officia ea nesciunt dolor. Deserunt cum excepturi explicabo amet perspiciatis alias corporis ratione veritatis nobis sapiente deleniti, ex voluptates, ipsum temporibus magnam voluptatum aspernatur harum.</p>
        <br>
    </div>
</template>

<style scoped>
    .container {
        background-color: var(--container-bg-color);
        padding: 2rem;
        width: 100%;
        max-width: 800px;
        margin: 5rem auto;
        border-radius: 5px;
    }

    .container > h1 {
        margin-top: .5rem;
        margin-bottom: 2rem;
        text-align: center;
    }

    .img-container {
        width: 100%;
        max-width: 400px;
        margin: 1rem;
        transform: translateX(0);
        opacity: 1;
        transition: all .5s ease;
    }

    .float-left {
        float: left;
    }

    .float-right {
        float: right;
    }

    .hidden-left {
        transform: translateX(-70%);
        opacity: 0;
    }

    .hidden-right {
        transform: translateX(70%);
        opacity: 0;
    }
</style>