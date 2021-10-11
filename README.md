# add mvc and routing
<b>//using add</b><br>
<pre>
using Microsoft.AspNetCore.Mvc;<br><br>
</pre>
//services add<br><br>
//Mvc projemize eklemek için AddMvc
<pre>
        public void ConfigureServices(IServiceCollection services)
        {
            services.AddMvc()
                .SetCompatibilityVersion(CompatibilityVersion.Version_2_2);
        }
        </pre>

//routing add<br>
            //localhost:5000/course/list<br>
            //localhost:5000/course/details/5<br>
            //localhost:5000/contorller/action/id<br>

            app.UseMvc(
                routes =>
                {
                    routes.MapRoute(
                        name: "Default",
                        template: "{controller}/{action}/{id}"
                        );
                });
