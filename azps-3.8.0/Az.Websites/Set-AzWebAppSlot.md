---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997303"
---
# <span data-ttu-id="0a001-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a001-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="0a001-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a001-102">SYNOPSIS</span></span>
<span data-ttu-id="0a001-103">Ändert einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="0a001-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="0a001-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a001-104">SYNTAX</span></span>

### <span data-ttu-id="0a001-105">S1</span><span class="sxs-lookup"><span data-stu-id="0a001-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a001-106">S2</span><span class="sxs-lookup"><span data-stu-id="0a001-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a001-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a001-107">DESCRIPTION</span></span>
<span data-ttu-id="0a001-108">Das Cmdlet " **Set-AzWebApp** " legt einen Azure Web App-Steckplatz fest.</span><span class="sxs-lookup"><span data-stu-id="0a001-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="0a001-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a001-109">EXAMPLES</span></span>

### <span data-ttu-id="0a001-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a001-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="0a001-111">Mit diesem Befehl wird der Appservice-Plan geändert, der dem Slot001 zugeordnet ist, und zwar auf dem ContosoWebApp, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0a001-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="0a001-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des Appservice-Plans und der zugehörigen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0a001-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="0a001-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="0a001-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="0a001-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0a001-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="0a001-115">Mit diesem Befehl wird HttpLoggingEnabled auf "true" festgelegt, wenn der Slot Slot001 in Bezug auf Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind-Web-westus</span><span class="sxs-lookup"><span data-stu-id="0a001-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="0a001-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a001-116">PARAMETERS</span></span>

### <span data-ttu-id="0a001-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="0a001-117">-AlwaysOn</span></span>
<span data-ttu-id="0a001-118">Stellen Sie sicher, dass die Web-App immer geladen wird, nachdem Sie inaktiv war.</span><span class="sxs-lookup"><span data-stu-id="0a001-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="0a001-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0a001-119">-AppServicePlan</span></span>
<span data-ttu-id="0a001-120">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="0a001-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="0a001-121">-AppSettings</span></span>
<span data-ttu-id="0a001-122">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0a001-122">App Settings HashTable.</span></span> <span data-ttu-id="0a001-123">Vorhandene App-Einstellungen werden ersetzt, wobei alle nicht bereitgestellten Einstellungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0a001-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a001-124">-AsJob</span></span>
<span data-ttu-id="0a001-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0a001-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a001-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0a001-126">-AssignIdentity</span></span>
<span data-ttu-id="0a001-127">Aktivieren/Deaktivieren von MSI für einen vorhandenen Steckplatz [Preview]</span><span class="sxs-lookup"><span data-stu-id="0a001-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="0a001-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="0a001-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="0a001-129">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="0a001-129">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="0a001-130">-AzureStoragePath</span></span>
<span data-ttu-id="0a001-131">Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0a001-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="0a001-132">Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="0a001-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="0a001-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="0a001-133">-ConnectionStrings</span></span>
<span data-ttu-id="0a001-134">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="0a001-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="0a001-135">-ContainerImageName</span></span>
<span data-ttu-id="0a001-136">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="0a001-136">Container Image Name</span></span>

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

### <span data-ttu-id="0a001-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="0a001-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="0a001-138">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="0a001-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="0a001-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="0a001-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="0a001-140">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="0a001-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="0a001-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="0a001-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="0a001-142">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="0a001-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="0a001-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="0a001-143">-DefaultDocuments</span></span>
<span data-ttu-id="0a001-144">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="0a001-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a001-145">-DefaultProfile</span></span>
<span data-ttu-id="0a001-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a001-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a001-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0a001-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="0a001-148">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0a001-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="0a001-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="0a001-150">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="0a001-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="0a001-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="0a001-151">-FtpsState</span></span>
<span data-ttu-id="0a001-152">Setzen Sie den Wert für den Zustand "FTP" für eine APP.</span><span class="sxs-lookup"><span data-stu-id="0a001-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="0a001-153">Zulässige Werte [alle erlaubt | Deaktiviert | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="0a001-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="0a001-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="0a001-154">-HandlerMappings</span></span>
<span data-ttu-id="0a001-155">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="0a001-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0a001-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="0a001-157">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0a001-157">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0a001-158">-HttpsOnly</span></span>
<span data-ttu-id="0a001-159">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einem vorhandenen Steckplatz</span><span class="sxs-lookup"><span data-stu-id="0a001-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="0a001-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="0a001-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="0a001-161">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="0a001-161">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0a001-162">-MinTlsVersion</span></span>
<span data-ttu-id="0a001-163">Die für SSL-Anforderungen erforderliche minimale Version von TLS.</span><span class="sxs-lookup"><span data-stu-id="0a001-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="0a001-164">Zulässige Werte [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="0a001-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="0a001-165">-Name</span><span class="sxs-lookup"><span data-stu-id="0a001-165">-Name</span></span>
<span data-ttu-id="0a001-166">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0a001-166">WebApp Name</span></span>

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

### <span data-ttu-id="0a001-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="0a001-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="0a001-168">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="0a001-168">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="0a001-169">-NumberOfWorkers</span></span>
<span data-ttu-id="0a001-170">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="0a001-170">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="0a001-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="0a001-171">-PhpVersion</span></span>
<span data-ttu-id="0a001-172">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="0a001-172">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="0a001-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="0a001-174">Anforderungs Ablaufverfolgung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0a001-174">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a001-175">-ResourceGroupName</span></span>
<span data-ttu-id="0a001-176">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0a001-176">Resource Group Name</span></span>

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

### <span data-ttu-id="0a001-177">-Slot</span><span class="sxs-lookup"><span data-stu-id="0a001-177">-Slot</span></span>
<span data-ttu-id="0a001-178">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="0a001-178">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="0a001-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="0a001-180">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="0a001-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a001-181">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="0a001-181">-WebApp</span></span>
<span data-ttu-id="0a001-182">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="0a001-182">WebApp Object</span></span>

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

### <span data-ttu-id="0a001-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="0a001-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="0a001-184">Web Sockets enabled Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0a001-184">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="0a001-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a001-185">CommonParameters</span></span>
<span data-ttu-id="0a001-186">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a001-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a001-187">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a001-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a001-188">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a001-188">INPUTS</span></span>

### <span data-ttu-id="0a001-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0a001-189">System.Int32</span></span>

### <span data-ttu-id="0a001-190">System. String</span><span class="sxs-lookup"><span data-stu-id="0a001-190">System.String</span></span>

### <span data-ttu-id="0a001-191">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0a001-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0a001-192">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a001-192">OUTPUTS</span></span>

### <span data-ttu-id="0a001-193">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0a001-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0a001-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a001-194">NOTES</span></span>

## <span data-ttu-id="0a001-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a001-195">RELATED LINKS</span></span>

[<span data-ttu-id="0a001-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a001-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="0a001-197">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a001-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="0a001-198">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a001-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="0a001-199">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a001-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="0a001-200">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a001-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="0a001-201">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a001-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="0a001-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0a001-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
