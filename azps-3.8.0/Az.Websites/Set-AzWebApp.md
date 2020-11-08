---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 75ee07a9ce74f5b2667d8197ca141883508faa1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003108"
---
# <span data-ttu-id="3f85d-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f85d-101">Set-AzWebApp</span></span>

## <span data-ttu-id="3f85d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f85d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f85d-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="3f85d-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="3f85d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f85d-104">SYNTAX</span></span>

### <span data-ttu-id="3f85d-105">S1</span><span class="sxs-lookup"><span data-stu-id="3f85d-105">S1</span></span>
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
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f85d-106">S2</span><span class="sxs-lookup"><span data-stu-id="3f85d-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f85d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f85d-107">DESCRIPTION</span></span>
<span data-ttu-id="3f85d-108">Das Cmdlet " **Set-AzWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="3f85d-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="3f85d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f85d-109">EXAMPLES</span></span>

### <span data-ttu-id="3f85d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f85d-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="3f85d-111">Mit diesem Befehl wird der Appservice-Plan geändert, der dem Web-App-ContosoWebApp zugeordnet ist, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3f85d-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="3f85d-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des Appservice-Plans und der zugehörigen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3f85d-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="3f85d-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="3f85d-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="3f85d-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3f85d-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="3f85d-115">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="3f85d-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3f85d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f85d-116">PARAMETERS</span></span>

### <span data-ttu-id="3f85d-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="3f85d-117">-AlwaysOn</span></span>
<span data-ttu-id="3f85d-118">Stellen Sie sicher, dass die Web-App immer geladen wird, nachdem Sie inaktiv war.</span><span class="sxs-lookup"><span data-stu-id="3f85d-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="3f85d-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3f85d-119">-AppServicePlan</span></span>
<span data-ttu-id="3f85d-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="3f85d-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="3f85d-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="3f85d-121">-AppSettings</span></span>
<span data-ttu-id="3f85d-122">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="3f85d-122">App Settings HashTable.</span></span> <span data-ttu-id="3f85d-123">Vorhandene App-Einstellungen werden ersetzt, wobei alle nicht bereitgestellten Einstellungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3f85d-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="3f85d-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f85d-124">-AsJob</span></span>
<span data-ttu-id="3f85d-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3f85d-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f85d-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3f85d-126">-AssignIdentity</span></span>
<span data-ttu-id="3f85d-127">Aktivieren/Deaktivieren von MSI für eine vorhandene Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="3f85d-127">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="3f85d-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="3f85d-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="3f85d-129">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="3f85d-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="3f85d-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="3f85d-130">-AzureStoragePath</span></span>
<span data-ttu-id="3f85d-131">Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f85d-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="3f85d-132">Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="3f85d-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="3f85d-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="3f85d-133">-ConnectionStrings</span></span>
<span data-ttu-id="3f85d-134">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="3f85d-134">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="3f85d-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="3f85d-135">-ContainerImageName</span></span>
<span data-ttu-id="3f85d-136">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="3f85d-136">Container Image Name</span></span>

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

### <span data-ttu-id="3f85d-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="3f85d-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="3f85d-138">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="3f85d-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="3f85d-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="3f85d-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="3f85d-140">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="3f85d-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="3f85d-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="3f85d-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="3f85d-142">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="3f85d-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="3f85d-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="3f85d-143">-DefaultDocuments</span></span>
<span data-ttu-id="3f85d-144">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="3f85d-144">Default Documents String Array</span></span>

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

### <span data-ttu-id="3f85d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f85d-145">-DefaultProfile</span></span>
<span data-ttu-id="3f85d-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f85d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f85d-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3f85d-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="3f85d-148">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="3f85d-148">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="3f85d-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="3f85d-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="3f85d-150">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="3f85d-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="3f85d-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="3f85d-151">-FtpsState</span></span>
<span data-ttu-id="3f85d-152">Setzen Sie den Wert für den Zustand "FTP" für eine APP.</span><span class="sxs-lookup"><span data-stu-id="3f85d-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="3f85d-153">Zulässige Werte [alle erlaubt | Deaktiviert | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="3f85d-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="3f85d-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="3f85d-154">-HandlerMappings</span></span>
<span data-ttu-id="3f85d-155">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="3f85d-155">Handler Mappings IList</span></span>

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

### <span data-ttu-id="3f85d-156">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="3f85d-156">-HostNames</span></span>
<span data-ttu-id="3f85d-157">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="3f85d-157">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="3f85d-158">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3f85d-158">-HttpLoggingEnabled</span></span>
<span data-ttu-id="3f85d-159">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="3f85d-159">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="3f85d-160">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3f85d-160">-HttpsOnly</span></span>
<span data-ttu-id="3f85d-161">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einer vorhandenen Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="3f85d-161">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="3f85d-162">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="3f85d-162">-ManagedPipelineMode</span></span>
<span data-ttu-id="3f85d-163">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="3f85d-163">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="3f85d-164">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3f85d-164">-MinTlsVersion</span></span>
<span data-ttu-id="3f85d-165">Die für SSL-Anforderungen erforderliche minimale Version von TLS.</span><span class="sxs-lookup"><span data-stu-id="3f85d-165">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="3f85d-166">Zulässige Werte [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="3f85d-166">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="3f85d-167">-Name</span><span class="sxs-lookup"><span data-stu-id="3f85d-167">-Name</span></span>
<span data-ttu-id="3f85d-168">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="3f85d-168">WebApp Name</span></span>

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

### <span data-ttu-id="3f85d-169">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="3f85d-169">-NetFrameworkVersion</span></span>
<span data-ttu-id="3f85d-170">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="3f85d-170">Net Framework Version</span></span>

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

### <span data-ttu-id="3f85d-171">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="3f85d-171">-NumberOfWorkers</span></span>
<span data-ttu-id="3f85d-172">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="3f85d-172">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="3f85d-173">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="3f85d-173">-PhpVersion</span></span>
<span data-ttu-id="3f85d-174">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="3f85d-174">Php Version</span></span>

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

### <span data-ttu-id="3f85d-175">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="3f85d-175">-RequestTracingEnabled</span></span>
<span data-ttu-id="3f85d-176">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="3f85d-176">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="3f85d-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f85d-177">-ResourceGroupName</span></span>
<span data-ttu-id="3f85d-178">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3f85d-178">Resource Group Name</span></span>

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

### <span data-ttu-id="3f85d-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="3f85d-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="3f85d-180">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="3f85d-180">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="3f85d-181">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="3f85d-181">-WebApp</span></span>
<span data-ttu-id="3f85d-182">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="3f85d-182">WebApp Object</span></span>

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

### <span data-ttu-id="3f85d-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="3f85d-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="3f85d-184">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="3f85d-184">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="3f85d-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f85d-185">CommonParameters</span></span>
<span data-ttu-id="3f85d-186">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f85d-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f85d-187">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f85d-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f85d-188">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f85d-188">INPUTS</span></span>

### <span data-ttu-id="3f85d-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3f85d-189">System.Int32</span></span>

### <span data-ttu-id="3f85d-190">System. String</span><span class="sxs-lookup"><span data-stu-id="3f85d-190">System.String</span></span>

### <span data-ttu-id="3f85d-191">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3f85d-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3f85d-192">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f85d-192">OUTPUTS</span></span>

### <span data-ttu-id="3f85d-193">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3f85d-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3f85d-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f85d-194">NOTES</span></span>

## <span data-ttu-id="3f85d-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f85d-195">RELATED LINKS</span></span>

[<span data-ttu-id="3f85d-196">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f85d-196">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3f85d-197">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f85d-197">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3f85d-198">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f85d-198">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3f85d-199">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f85d-199">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3f85d-200">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f85d-200">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="3f85d-201">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f85d-201">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
