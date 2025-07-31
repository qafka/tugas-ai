import Link from "next/link"
import Image from "next/image"
import { Button } from "@/components/ui/button"
import { Card, CardContent, CardDescription, CardFooter, CardHeader, CardTitle } from "@/components/ui/card"
import {
  CheckCircle,
  Users,
  BarChart,
  Workflow,
  Lock,
  Star,
  Twitter,
  Facebook,
  Linkedin,
  Instagram,
  Mail,
} from "lucide-react"

export default function Component() {
  return (
    <div className="flex flex-col min-h-[100dvh]">
      {/* Header */}
      <header className="px-4 lg:px-6 h-14 flex items-center border-b">
        <Link href="#" className="flex items-center justify-center gap-2">
          <CheckCircle className="h-6 w-6 text-primary" />
          <span className="text-lg font-bold">StreamLine</span>
        </Link>
        <nav className="ml-auto hidden md:flex gap-6">
          <Link href="#features" className="text-sm font-medium hover:underline underline-offset-4">
            Features
          </Link>
          <Link href="#testimonials" className="text-sm font-medium hover:underline underline-offset-4">
            Testimonials
          </Link>
          <Link href="#pricing" className="text-sm font-medium hover:underline underline-offset-4">
            Pricing
          </Link>
          <Link href="#contact" className="text-sm font-medium hover:underline underline-offset-4">
            Contact
          </Link>
        </nav>
        <Button asChild className="ml-auto md:ml-6">
          <Link href="#signup">Sign Up</Link>
        </Button>
      </header>

      <main className="flex-1">
        {/* Hero Section */}
        <section className="w-full py-12 md:py-24 lg:py-32 xl:py-48 bg-gradient-to-r from-gray-50 to-white">
          <div className="container px-4 md:px-6">
            <div className="grid gap-6 lg:grid-cols-[1fr_550px] lg:gap-12 xl:grid-cols-[1fr_650px] items-center">
              <div className="flex flex-col justify-center space-y-4">
                <div className="space-y-2">
                  <h1 className="text-3xl font-bold tracking-tighter sm:text-5xl xl:text-6xl/none">
                    Streamline Your Workflow, Amplify Your Success.
                  </h1>
                  <p className="max-w-[600px] text-muted-foreground md:text-xl">
                    Empower your team with StreamLine's intuitive platform designed to boost productivity and foster
                    seamless collaboration.
                  </p>
                </div>
                <div className="flex flex-col gap-2 min-[400px]:flex-row">
                  <Button asChild>
                    <Link href="#signup">Get Started</Link>
                  </Button>
                  <Button asChild variant="outline">
                    <Link href="#features">Learn More</Link>
                  </Button>
                </div>
              </div>
              <Image
                src="/placeholder.svg?height=550&width=650"
                width="650"
                height="550"
                alt="Hero"
                className="mx-auto aspect-[16/9] overflow-hidden rounded-xl object-cover sm:w-full lg:order-last"
              />
            </div>
          </div>
        </section>

        {/* Features Section */}
        <section id="features" className="w-full py-12 md:py-24 lg:py-32 bg-muted">
          <div className="container px-4 md:px-6">
            <div className="flex flex-col items-center justify-center space-y-4 text-center">
              <div className="space-y-2">
                <h2 className="text-3xl font-bold tracking-tighter sm:text-5xl">Unlock Your Team's Full Potential</h2>
                <p className="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
                  StreamLine provides powerful features to help you work smarter, not harder.
                </p>
              </div>
            </div>
            <div className="mx-auto grid max-w-5xl items-start gap-8 py-12 sm:grid-cols-2 md:gap-12 lg:grid-cols-4">
              <div className="grid gap-1 text-center">
                <div className="flex justify-center mb-2">
                  <Users className="h-10 w-10 text-primary" />
                </div>
                <h3 className="text-lg font-bold">Collaborative Workspaces</h3>
                <p className="text-sm text-muted-foreground">
                  Work together in real-time, share documents, and manage projects seamlessly.
                </p>
              </div>
              <div className="grid gap-1 text-center">
                <div className="flex justify-center mb-2">
                  <BarChart className="h-10 w-10 text-primary" />
                </div>
                <h3 className="text-lg font-bold">Advanced Analytics</h3>
                <p className="text-sm text-muted-foreground">
                  Gain deep insights into your performance with customizable dashboards and reports.
                </p>
              </div>
              <div className="grid gap-1 text-center">
                <div className="flex justify-center mb-2">
                  <Workflow className="h-10 w-10 text-primary" />
                </div>
                <h3 className="text-lg font-bold">Automated Workflows</h3>
                <p className="text-sm text-muted-foreground">
                  Automate repetitive tasks and integrate with your favorite tools to save time.
                </p>
              </div>
              <div className="grid gap-1 text-center">
                <div className="flex justify-center mb-2">
                  <Lock className="h-10 w-10 text-primary" />
                </div>
                <h3 className="text-lg font-bold">Secure Data Management</h3>
                <p className="text-sm text-muted-foreground">
                  Your data is protected with industry-leading security protocols and regular backups.
                </p>
              </div>
            </div>
          </div>
        </section>

        {/* Testimonials Section */}
        <section id="testimonials" className="w-full py-12 md:py-24 lg:py-32">
          <div className="container px-4 md:px-6">
            <div className="flex flex-col items-center justify-center space-y-4 text-center">
              <div className="space-y-2">
                <h2 className="text-3xl font-bold tracking-tighter sm:text-5xl">What Our Customers Say</h2>
                <p className="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
                  Hear from businesses that have transformed their operations with StreamLine.
                </p>
              </div>
            </div>
            <div className="mx-auto grid max-w-5xl items-start gap-8 py-12 sm:grid-cols-2 lg:grid-cols-3">
              <Card className="flex flex-col h-full">
                <CardContent className="flex-1 p-6">
                  <div className="flex items-center gap-1 mb-4">
                    {[...Array(5)].map((_, i) => (
                      <Star key={i} className="h-5 w-5 fill-yellow-400 text-yellow-400" />
                    ))}
                  </div>
                  <p className="text-lg leading-relaxed">
                    &quot;StreamLine has revolutionized how our team collaborates. We&apos;ve seen a significant boost
                    in productivity since implementing it.&quot;
                  </p>
                </CardContent>
                <CardFooter className="p-6 pt-0">
                  <div className="flex items-center gap-3">
                    <Image
                      src="/placeholder.svg?height=48&width=48"
                      width="48"
                      height="48"
                      alt="Avatar"
                      className="rounded-full object-cover"
                    />
                    <div>
                      <p className="font-semibold">Jane Doe</p>
                      <p className="text-sm text-muted-foreground">CEO, Tech Solutions</p>
                    </div>
                  </div>
                </CardFooter>
              </Card>
              <Card className="flex flex-col h-full">
                <CardContent className="flex-1 p-6">
                  <div className="flex items-center gap-1 mb-4">
                    {[...Array(5)].map((_, i) => (
                      <Star key={i} className="h-5 w-5 fill-yellow-400 text-yellow-400" />
                    ))}
                  </div>
                  <p className="text-lg leading-relaxed">
                    &quot;The analytics features are a game-changer. We now make data-driven decisions with ease,
                    leading to better outcomes.&quot;
                  </p>
                </CardContent>
                <CardFooter className="p-6 pt-0">
                  <div className="flex items-center gap-3">
                    <Image
                      src="/placeholder.svg?height=48&width=48"
                      width="48"
                      height="48"
                      alt="Avatar"
                      className="rounded-full object-cover"
                    />
                    <div>
                      <p className="font-semibold">John Smith</p>
                      <p className="text-sm text-muted-foreground">Marketing Director, Global Corp</p>
                    </div>
                  </div>
                </CardFooter>
              </Card>
              <Card className="flex flex-col h-full">
                <CardContent className="flex-1 p-6">
                  <div className="flex items-center gap-1 mb-4">
                    {[...Array(5)].map((_, i) => (
                      <Star key={i} className="h-5 w-5 fill-yellow-400 text-yellow-400" />
                    ))}
                  </div>
                  <p className="text-lg leading-relaxed">
                    &quot;Automated workflows have saved us countless hours. StreamLine is an essential tool for our
                    daily operations.&quot;
                  </p>
                </CardContent>
                <CardFooter className="p-6 pt-0">
                  <div className="flex items-center gap-3">
                    <Image
                      src="/placeholder.svg?height=48&width=48"
                      width="48"
                      height="48"
                      alt="Avatar"
                      className="rounded-full object-cover"
                    />
                    <div>
                      <p className="font-semibold">Sarah Lee</p>
                      <p className="text-sm text-muted-foreground">Operations Manager, Innovate Co.</p>
                    </div>
                  </div>
                </CardFooter>
              </Card>
            </div>
          </div>
        </section>

        {/* Pricing Section */}
        <section id="pricing" className="w-full py-12 md:py-24 lg:py-32 bg-muted">
          <div className="container px-4 md:px-6">
            <div className="flex flex-col items-center justify-center space-y-4 text-center">
              <div className="space-y-2">
                <h2 className="text-3xl font-bold tracking-tighter sm:text-5xl">Simple, Transparent Pricing</h2>
                <p className="max-w-[900px] text-muted-foreground md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
                  Choose the plan that best fits your team&apos;s needs and scale as you grow.
                </p>
              </div>
            </div>
            <div className="mx-auto grid max-w-5xl items-start gap-8 py-12 sm:grid-cols-2 lg:grid-cols-3">
              <Card className="flex flex-col h-full">
                <CardHeader className="pb-4">
                  <CardTitle className="text-2xl font-bold">Basic</CardTitle>
                  <CardDescription>Perfect for individuals and small teams.</CardDescription>
                </CardHeader>
                <CardContent className="flex-1">
                  <div className="text-4xl font-bold mb-4">
                    $19<span className="text-base font-normal">/month</span>
                  </div>
                  <ul className="space-y-2 text-muted-foreground">
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>5 Users</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>10 GB Storage</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Basic Analytics</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Email Support</span>
                    </li>
                  </ul>
                </CardContent>
                <CardFooter className="pt-4">
                  <Button className="w-full">Choose Basic</Button>
                </CardFooter>
              </Card>
              <Card className="flex flex-col h-full border-2 border-primary">
                <CardHeader className="pb-4">
                  <CardTitle className="text-2xl font-bold">Pro</CardTitle>
                  <CardDescription>Ideal for growing teams and advanced features.</CardDescription>
                </CardHeader>
                <CardContent className="flex-1">
                  <div className="text-4xl font-bold mb-4">
                    $49<span className="text-base font-normal">/month</span>
                  </div>
                  <ul className="space-y-2 text-muted-foreground">
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Unlimited Users</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>100 GB Storage</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Advanced Analytics</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Automated Workflows</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Priority Support</span>
                    </li>
                  </ul>
                </CardContent>
                <CardFooter className="pt-4">
                  <Button className="w-full">Choose Pro</Button>
                </CardFooter>
              </Card>
              <Card className="flex flex-col h-full">
                <CardHeader className="pb-4">
                  <CardTitle className="text-2xl font-bold">Enterprise</CardTitle>
                  <CardDescription>Custom solutions for large organizations.</CardDescription>
                </CardHeader>
                <CardContent className="flex-1">
                  <div className="text-4xl font-bold mb-4">Custom</div>
                  <ul className="space-y-2 text-muted-foreground">
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Dedicated Support</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Unlimited Storage</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>Custom Integrations</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>On-premise Options</span>
                    </li>
                    <li className="flex items-center gap-2">
                      <CheckCircle className="h-4 w-4 text-primary" />
                      <span>SLA Guaranteed</span>
                    </li>
                  </ul>
                </CardContent>
                <CardFooter className="pt-4">
                  <Button className="w-full bg-transparent" variant="outline">
                    Contact Sales
                  </Button>
                </CardFooter>
              </Card>
            </div>
          </div>
        </section>

        {/* Final Call-to-Action Section */}
        <section id="signup" className="w-full py-12 md:py-24 lg:py-32 bg-primary text-primary-foreground">
          <div className="container grid items-center justify-center gap-4 px-4 text-center md:px-6">
            <div className="space-y-3">
              <h2 className="text-3xl font-bold tracking-tighter md:text-4xl/tight">
                Ready to Transform Your Business?
              </h2>
              <p className="mx-auto max-w-[600px] md:text-xl/relaxed lg:text-base/relaxed xl:text-xl/relaxed">
                Join thousands of successful teams who are already streamlining their operations with StreamLine.
              </p>
            </div>
            <div className="flex flex-col gap-2 min-[400px]:flex-row justify-center">
              <Button asChild size="lg" className="bg-primary-foreground text-primary hover:bg-primary-foreground/90">
                <Link href="#signup">Start Your Free Trial</Link>
              </Button>
              <Button
                asChild
                size="lg"
                variant="outline"
                className="border-primary-foreground text-primary-foreground hover:bg-primary-foreground/10 bg-transparent"
              >
                <Link href="#contact">Contact Sales</Link>
              </Button>
            </div>
          </div>
        </section>
      </main>

      {/* Footer */}
      <footer className="flex flex-col gap-4 sm:flex-row py-6 w-full shrink-0 items-center px-4 md:px-6 border-t">
        <p className="text-xs text-muted-foreground">
          &copy; {new Date().getFullYear()} StreamLine. All rights reserved.
        </p>
        <nav className="sm:ml-auto flex gap-4 sm:gap-6">
          <Link href="#" className="text-xs hover:underline underline-offset-4">
            Privacy Policy
          </Link>
          <Link href="#" className="text-xs hover:underline underline-offset-4">
            Terms of Service
          </Link>
          <Link href="#" className="text-xs hover:underline underline-offset-4">
            Support
          </Link>
        </nav>
        <div className="flex gap-4 sm:ml-4">
          <Link href="#" aria-label="Twitter">
            <Twitter className="h-5 w-5 text-muted-foreground hover:text-primary" />
          </Link>
          <Link href="#" aria-label="Facebook">
            <Facebook className="h-5 w-5 text-muted-foreground hover:text-primary" />
          </Link>
          <Link href="#" aria-label="LinkedIn">
            <Linkedin className="h-5 w-5 text-muted-foreground hover:text-primary" />
          </Link>
          <Link href="#" aria-label="Instagram">
            <Instagram className="h-5 w-5 text-muted-foreground hover:text-primary" />
          </Link>
          <Link href="#" aria-label="Email">
            <Mail className="h-5 w-5 text-muted-foreground hover:text-primary" />
          </Link>
        </div>
      </footer>
    </div>
  )
}
