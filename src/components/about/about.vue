<template>
    <div class="container">
        <div class="row my-5 align-items-center">
            <div class="col-md-7">
                <h2 class="h1-responsive">
                    I'm <mark style="color:red">{{ portfolioData.name }}</mark>
                </h2>
                <br><hr><br>
                <p class="text-muted">{{ portfolioData.about }}</p>
                <p class="text-muted">
                    <i class="fab fa-github"></i> &nbsp;
                    <i class="fab fa-linkedin-in"></i> &nbsp;
                    <i class="fab fa-facebook-f"></i> &nbsp;
                </p>
                <a href="../../assets/resume/Varsha_Resume.pdf" class="btn btn-outline-primary" download="Varsha_Resume.pdf">Download Resume</a>
            </div>
            <div class="col-md-5">
                <img src="https://gdgjalandhar.com/img/varsha.380e53ce.jpg" class="rounded-circle" width="50%" alt="" srcset="">
            </div>
        </div>
    </div>
</template>

<script>
import portfolioData from '@/assets/data/portfolioData.json'
export default {
    data() {
        return {
            portfolioData
        }
    }
}
</script>


