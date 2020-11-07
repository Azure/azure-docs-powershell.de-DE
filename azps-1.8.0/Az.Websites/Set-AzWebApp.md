---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658504"
---
# <span data-ttu-id="2b835-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2b835-101">Set-AzWebApp</span></span>



## <span data-ttu-id="2b835-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b835-102">SYNOPSIS</span></span>

<span data-ttu-id="2b835-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2b835-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="2b835-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b835-104">SYNTAX</span></span>



### <span data-ttu-id="2b835-105">S1</span><span class="sxs-lookup"><span data-stu-id="2b835-105">S1</span></span>

```

Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]

 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]

 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]

 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]

 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]

 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]

 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]

 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]

 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]

 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



### <span data-ttu-id="2b835-106">S2</span><span class="sxs-lookup"><span data-stu-id="2b835-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="2b835-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b835-107">DESCRIPTION</span></span>

<span data-ttu-id="2b835-108">Das Cmdlet " **Set-AzWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="2b835-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="2b835-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b835-109">EXAMPLES</span></span>



### <span data-ttu-id="2b835-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2b835-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="2b835-111">Mit diesem Befehl wird der Appservice-Plan geändert, der dem Web-App-ContosoWebApp zugeordnet ist, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2b835-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="2b835-112">Verwenden Sie den Link zu learm, um mehr über das Ändern des Appservice-Plans und die damit verbundenen Einschränkungen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="2b835-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="2b835-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2b835-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="2b835-114">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="2b835-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="2b835-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b835-115">PARAMETERS</span></span>



### <span data-ttu-id="2b835-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b835-116">-AppServicePlan</span></span>

<span data-ttu-id="2b835-117">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="2b835-117">App Service Plan Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 2

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="2b835-118">-AppSettings</span></span>

<span data-ttu-id="2b835-119">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2b835-119">App Settings HashTable</span></span>



```yaml

Type: System.Collections.Hashtable

Parameter Sets: S1

Aliases:



Required: False

Position: 9

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b835-120">-AsJob</span></span>

<span data-ttu-id="2b835-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2b835-121">Run cmdlet in the background</span></span>



```yaml

Type: System.Management.Automation.SwitchParameter

Parameter Sets: (All)

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2b835-122">-AssignIdentity</span></span>

<span data-ttu-id="2b835-123">Aktivieren/Deaktivieren von MSI für eine vorhandene Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="2b835-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="2b835-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="2b835-125">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="2b835-125">Destination slot name for auto swap</span></span>



```yaml

Type: System.String

Parameter Sets: (All)

Aliases:



Required: False

Position: 15

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="2b835-126">-AzureStoragePath</span></span>

<span data-ttu-id="2b835-127">Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b835-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="2b835-128">Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="2b835-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



```yaml

Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="2b835-129">-ConnectionStrings</span></span>

<span data-ttu-id="2b835-130">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2b835-130">Connection Strings HashTable</span></span>



```yaml

Type: System.Collections.Hashtable

Parameter Sets: S1

Aliases:



Required: False

Position: 10

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-131">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="2b835-131">-ContainerImageName</span></span>

<span data-ttu-id="2b835-132">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="2b835-132">Container Image Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="2b835-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="2b835-134">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="2b835-134">Private Container Registry Password</span></span>



```yaml

Type: System.Security.SecureString

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="2b835-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="2b835-136">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="2b835-136">Private Container Registry Server Url</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="2b835-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="2b835-138">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="2b835-138">Private Container Registry Username</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-139">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="2b835-139">-DefaultDocuments</span></span>

<span data-ttu-id="2b835-140">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="2b835-140">Default Documents String Array</span></span>



```yaml

Type: System.String[]

Parameter Sets: S1

Aliases:



Required: False

Position: 3

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b835-141">-DefaultProfile</span></span>

<span data-ttu-id="2b835-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b835-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



```yaml

Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer

Parameter Sets: (All)

Aliases: AzContext, AzureRmContext, AzureCredential



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2b835-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="2b835-144">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="2b835-144">Detailed Error Logging Enabled Boolean</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 8

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="2b835-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="2b835-146">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="2b835-146">Enables/Disables container continuous deployment webhook</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="2b835-147">-HandlerMappings</span></span>

<span data-ttu-id="2b835-148">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="2b835-148">Handler Mappings IList</span></span>



```yaml

Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]

Parameter Sets: S1

Aliases:



Required: False

Position: 11

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-149">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="2b835-149">-HostNames</span></span>

<span data-ttu-id="2b835-150">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="2b835-150">WebApp HostNames String Array</span></span>



```yaml

Type: System.String[]

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2b835-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="2b835-152">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="2b835-152">HttpLoggingEnabled Boolean</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 7

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2b835-153">-HttpsOnly</span></span>

<span data-ttu-id="2b835-154">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einer vorhandenen Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="2b835-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="2b835-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="2b835-156">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="2b835-156">Managed Pipeline Mode Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:

Accepted values: Classic, Integrated



Required: False

Position: 12

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-157">-Name</span><span class="sxs-lookup"><span data-stu-id="2b835-157">-Name</span></span>

<span data-ttu-id="2b835-158">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="2b835-158">WebApp Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: True

Position: 1

Default value: None

Accept pipeline input: True (ByPropertyName)

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="2b835-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="2b835-160">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="2b835-160">Net Framework Version</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 4

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="2b835-161">-NumberOfWorkers</span></span>

<span data-ttu-id="2b835-162">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="2b835-162">The number of workers to be allocated</span></span>



```yaml

Type: System.Int32

Parameter Sets: (All)

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: True (ByValue)

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="2b835-163">-PhpVersion</span></span>

<span data-ttu-id="2b835-164">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="2b835-164">Php Version</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 5

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="2b835-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="2b835-166">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="2b835-166">Request Tracing Enabled</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 6

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b835-167">-ResourceGroupName</span></span>

<span data-ttu-id="2b835-168">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2b835-168">Resource Group Name</span></span>



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: True

Position: 0

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="2b835-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="2b835-170">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="2b835-170">Use 32-bit Worker Process Boolean</span></span>



```yaml

Type: System.Boolean

Parameter Sets: (All)

Aliases:



Required: False

Position: 14

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-171">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="2b835-171">-WebApp</span></span>

<span data-ttu-id="2b835-172">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="2b835-172">WebApp Object</span></span>



```yaml

Type: Microsoft.Azure.Commands.WebApps.Models.PSSite

Parameter Sets: S2

Aliases:



Required: True

Position: 0

Default value: None

Accept pipeline input: True (ByValue)

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="2b835-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="2b835-174">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="2b835-174">WebSocketsEnabled Boolean</span></span>



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 13

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### <span data-ttu-id="2b835-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b835-175">CommonParameters</span></span>

<span data-ttu-id="2b835-176">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b835-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b835-177">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b835-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="2b835-178">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b835-178">INPUTS</span></span>



### <span data-ttu-id="2b835-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2b835-179">System.Int32</span></span>



### <span data-ttu-id="2b835-180">System. String</span><span class="sxs-lookup"><span data-stu-id="2b835-180">System.String</span></span>



### <span data-ttu-id="2b835-181">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2b835-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="2b835-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b835-182">OUTPUTS</span></span>



### <span data-ttu-id="2b835-183">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2b835-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="2b835-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b835-184">NOTES</span></span>



## <span data-ttu-id="2b835-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b835-185">RELATED LINKS</span></span>



[<span data-ttu-id="2b835-186">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2b835-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="2b835-187">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2b835-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="2b835-188">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2b835-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="2b835-189">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2b835-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="2b835-190">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2b835-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="2b835-191">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2b835-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

