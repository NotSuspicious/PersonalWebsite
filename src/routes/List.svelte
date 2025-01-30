<script>
import SectionHeaderSmall from "./SectionHeader-small.svelte";
</script>

<div class="Skills">
    <SectionHeaderSmall text="SKILLS" />
    <div class="container">
        <div class="skill">
            <h3 class=" roboto-condensed-bold-italic">
                3D DEVELOPMENT
            </h3>
            <ul class="roboto-regular">
                <li>Unreal Engine 5</li>
                <li>Unity</li>
                <li>OpenGL</li>
                <li>Blender</li>
                <li>Maya</li>
                <li>Houdini</li>
            </ul>
        </div>

        <div class="skill ">
            <h3 class="roboto-condensed-bold-italic">
                TECHNICAL
            </h3>
            <ul class="roboto-regular">
                <li>C# 9</li>
                <li>C++ 11</li>
                <li>GLSL</li>
                <li>Python</li>
                <li>Perforce</li>
                <li>Git</li>
            </ul>
        </div>

        <div class="skill">
            <h3 class="roboto-condensed-bold-italic">
                SOFTWARE
            </h3>
            <ul class="roboto-regular">
                <li>Photoshop</li>
                <li>Premiere Pro</li>
                <li>Figma</li>
                <li>Notion</li>
                <li>Logic Pro</li>
            </ul>
        </div>
    </div>
</div>

<style>
    .container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 24px;
        margin: 24px 0 72px 0;
    }

    .skill {
        color: var(--orange);
    }

    @media (max-width: 992px) {
        .Skills {
            display: none;
        }
    }
</style>