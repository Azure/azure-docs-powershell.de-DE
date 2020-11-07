---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826679"
---
# <span data-ttu-id="65540-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65540-101">Set-AzWebApp</span></span>

## <span data-ttu-id="65540-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65540-102">SYNOPSIS</span></span>
<span data-ttu-id="65540-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="65540-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="65540-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65540-104">SYNTAX</span></span>

### <span data-ttu-id="65540-105">S1</span><span class="sxs-lookup"><span data-stu-id="65540-105">S1</span></span>
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

### <span data-ttu-id="65540-106">S2</span><span class="sxs-lookup"><span data-stu-id="65540-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65540-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65540-107">DESCRIPTION</span></span>
<span data-ttu-id="65540-108">Das Cmdlet " **Set-AzWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="65540-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="65540-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65540-109">EXAMPLES</span></span>

### <span data-ttu-id="65540-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65540-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="65540-111">Mit diesem Befehl wird der Appservice-Plan geändert, der dem Web-App-ContosoWebApp zugeordnet ist, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="65540-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="65540-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des Appservice-Plans und der zugehörigen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="65540-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="65540-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="65540-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="65540-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="65540-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="65540-115">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="65540-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="65540-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="65540-116">PARAMETERS</span></span>

### <span data-ttu-id="65540-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="65540-117">-AppServicePlan</span></span>
<span data-ttu-id="65540-118">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="65540-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="65540-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="65540-119">-AppSettings</span></span>
<span data-ttu-id="65540-120">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="65540-120">App Settings HashTable.</span></span> <span data-ttu-id="65540-121">Vorhandene App-Einstellungen werden ersetzt, wobei alle nicht bereitgestellten Einstellungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="65540-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="65540-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65540-122">-AsJob</span></span>
<span data-ttu-id="65540-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="65540-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65540-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="65540-124">-AssignIdentity</span></span>
<span data-ttu-id="65540-125">Aktivieren/Deaktivieren von MSI für eine vorhandene Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="65540-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="65540-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="65540-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="65540-127">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="65540-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="65540-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="65540-128">-AzureStoragePath</span></span>
<span data-ttu-id="65540-129">Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="65540-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="65540-130">Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="65540-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="65540-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="65540-131">-ConnectionStrings</span></span>
<span data-ttu-id="65540-132">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="65540-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="65540-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="65540-133">-ContainerImageName</span></span>
<span data-ttu-id="65540-134">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="65540-134">Container Image Name</span></span>

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

### <span data-ttu-id="65540-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="65540-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="65540-136">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="65540-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="65540-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="65540-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="65540-138">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="65540-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="65540-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="65540-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="65540-140">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="65540-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="65540-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="65540-141">-DefaultDocuments</span></span>
<span data-ttu-id="65540-142">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="65540-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="65540-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65540-143">-DefaultProfile</span></span>
<span data-ttu-id="65540-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65540-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65540-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="65540-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="65540-146">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="65540-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="65540-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="65540-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="65540-148">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="65540-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="65540-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="65540-149">-HandlerMappings</span></span>
<span data-ttu-id="65540-150">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="65540-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="65540-151">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="65540-151">-HostNames</span></span>
<span data-ttu-id="65540-152">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="65540-152">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="65540-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="65540-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="65540-154">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="65540-154">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="65540-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="65540-155">-HttpsOnly</span></span>
<span data-ttu-id="65540-156">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einer vorhandenen Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="65540-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="65540-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="65540-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="65540-158">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="65540-158">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="65540-159">-Name</span><span class="sxs-lookup"><span data-stu-id="65540-159">-Name</span></span>
<span data-ttu-id="65540-160">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="65540-160">WebApp Name</span></span>

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

### <span data-ttu-id="65540-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="65540-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="65540-162">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="65540-162">Net Framework Version</span></span>

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

### <span data-ttu-id="65540-163">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="65540-163">-NumberOfWorkers</span></span>
<span data-ttu-id="65540-164">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="65540-164">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="65540-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="65540-165">-PhpVersion</span></span>
<span data-ttu-id="65540-166">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="65540-166">Php Version</span></span>

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

### <span data-ttu-id="65540-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="65540-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="65540-168">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="65540-168">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="65540-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65540-169">-ResourceGroupName</span></span>
<span data-ttu-id="65540-170">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="65540-170">Resource Group Name</span></span>

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

### <span data-ttu-id="65540-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="65540-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="65540-172">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="65540-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="65540-173">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="65540-173">-WebApp</span></span>
<span data-ttu-id="65540-174">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="65540-174">WebApp Object</span></span>

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

### <span data-ttu-id="65540-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="65540-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="65540-176">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="65540-176">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="65540-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65540-177">CommonParameters</span></span>
<span data-ttu-id="65540-178">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65540-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65540-179">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65540-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65540-180">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65540-180">INPUTS</span></span>

### <span data-ttu-id="65540-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="65540-181">System.Int32</span></span>

### <span data-ttu-id="65540-182">System. String</span><span class="sxs-lookup"><span data-stu-id="65540-182">System.String</span></span>

### <span data-ttu-id="65540-183">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="65540-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="65540-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65540-184">OUTPUTS</span></span>

### <span data-ttu-id="65540-185">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="65540-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="65540-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="65540-186">NOTES</span></span>

## <span data-ttu-id="65540-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65540-187">RELATED LINKS</span></span>

[<span data-ttu-id="65540-188">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65540-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="65540-189">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65540-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="65540-190">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65540-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="65540-191">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65540-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="65540-192">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65540-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="65540-193">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="65540-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
