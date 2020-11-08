---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 0120bd19d1c8930129796e47758bd9f91dccfd5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009501"
---
# <span data-ttu-id="12ec6-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="12ec6-101">Set-AzWebApp</span></span>

## <span data-ttu-id="12ec6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="12ec6-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="12ec6-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="12ec6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12ec6-104">SYNTAX</span></span>

### <span data-ttu-id="12ec6-105">S1</span><span class="sxs-lookup"><span data-stu-id="12ec6-105">S1</span></span>
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

### <span data-ttu-id="12ec6-106">S2</span><span class="sxs-lookup"><span data-stu-id="12ec6-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12ec6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12ec6-107">DESCRIPTION</span></span>
<span data-ttu-id="12ec6-108">Das Cmdlet " **Set-AzWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="12ec6-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="12ec6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12ec6-109">EXAMPLES</span></span>

### <span data-ttu-id="12ec6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12ec6-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="12ec6-111">Mit diesem Befehl wird der Appservice-Plan geändert, der dem Web-App-ContosoWebApp zugeordnet ist, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="12ec6-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="12ec6-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des Appservice-Plans und der zugehörigen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="12ec6-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="12ec6-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="12ec6-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="12ec6-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="12ec6-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="12ec6-115">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="12ec6-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="12ec6-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="12ec6-116">Example 3</span></span>

<span data-ttu-id="12ec6-117">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="12ec6-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="12ec6-118">automatisch</span><span class="sxs-lookup"><span data-stu-id="12ec6-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="12ec6-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="12ec6-119">PARAMETERS</span></span>

### <span data-ttu-id="12ec6-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="12ec6-120">-AlwaysOn</span></span>
<span data-ttu-id="12ec6-121">Stellen Sie sicher, dass die Web-App immer geladen wird, nachdem Sie inaktiv war.</span><span class="sxs-lookup"><span data-stu-id="12ec6-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="12ec6-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="12ec6-122">-AppServicePlan</span></span>
<span data-ttu-id="12ec6-123">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="12ec6-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="12ec6-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="12ec6-124">-AppSettings</span></span>
<span data-ttu-id="12ec6-125">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="12ec6-125">App Settings HashTable.</span></span> <span data-ttu-id="12ec6-126">Vorhandene App-Einstellungen werden ersetzt, wobei alle nicht bereitgestellten Einstellungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="12ec6-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="12ec6-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12ec6-127">-AsJob</span></span>
<span data-ttu-id="12ec6-128">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="12ec6-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12ec6-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="12ec6-129">-AssignIdentity</span></span>
<span data-ttu-id="12ec6-130">Aktivieren/Deaktivieren von MSI für eine vorhandene Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="12ec6-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="12ec6-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="12ec6-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="12ec6-132">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="12ec6-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="12ec6-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="12ec6-133">-AzureStoragePath</span></span>
<span data-ttu-id="12ec6-134">Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="12ec6-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="12ec6-135">Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="12ec6-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="12ec6-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="12ec6-136">-ConnectionStrings</span></span>
<span data-ttu-id="12ec6-137">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="12ec6-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="12ec6-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="12ec6-138">-ContainerImageName</span></span>
<span data-ttu-id="12ec6-139">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="12ec6-139">Container Image Name</span></span>

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

### <span data-ttu-id="12ec6-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="12ec6-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="12ec6-141">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="12ec6-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="12ec6-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="12ec6-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="12ec6-143">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="12ec6-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="12ec6-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="12ec6-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="12ec6-145">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="12ec6-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="12ec6-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="12ec6-146">-DefaultDocuments</span></span>
<span data-ttu-id="12ec6-147">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="12ec6-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="12ec6-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ec6-148">-DefaultProfile</span></span>
<span data-ttu-id="12ec6-149">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12ec6-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12ec6-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="12ec6-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="12ec6-151">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="12ec6-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="12ec6-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="12ec6-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="12ec6-153">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="12ec6-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="12ec6-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="12ec6-154">-FtpsState</span></span>
<span data-ttu-id="12ec6-155">Setzen Sie den Wert für den Zustand "FTP" für eine APP.</span><span class="sxs-lookup"><span data-stu-id="12ec6-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="12ec6-156">Zulässige Werte [alle erlaubt | Deaktiviert | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="12ec6-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="12ec6-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="12ec6-157">-HandlerMappings</span></span>
<span data-ttu-id="12ec6-158">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="12ec6-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="12ec6-159">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="12ec6-159">-HostNames</span></span>
<span data-ttu-id="12ec6-160">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="12ec6-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="12ec6-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="12ec6-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="12ec6-162">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="12ec6-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="12ec6-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="12ec6-163">-HttpsOnly</span></span>
<span data-ttu-id="12ec6-164">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einer vorhandenen Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="12ec6-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="12ec6-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="12ec6-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="12ec6-166">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="12ec6-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="12ec6-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="12ec6-167">-MinTlsVersion</span></span>
<span data-ttu-id="12ec6-168">Die für SSL-Anforderungen erforderliche minimale Version von TLS.</span><span class="sxs-lookup"><span data-stu-id="12ec6-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="12ec6-169">Zulässige Werte [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="12ec6-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="12ec6-170">-Name</span><span class="sxs-lookup"><span data-stu-id="12ec6-170">-Name</span></span>
<span data-ttu-id="12ec6-171">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="12ec6-171">WebApp Name</span></span>

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

### <span data-ttu-id="12ec6-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="12ec6-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="12ec6-173">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="12ec6-173">Net Framework Version</span></span>

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

### <span data-ttu-id="12ec6-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="12ec6-174">-NumberOfWorkers</span></span>
<span data-ttu-id="12ec6-175">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="12ec6-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="12ec6-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="12ec6-176">-PhpVersion</span></span>
<span data-ttu-id="12ec6-177">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="12ec6-177">Php Version</span></span>

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

### <span data-ttu-id="12ec6-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="12ec6-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="12ec6-179">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="12ec6-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="12ec6-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ec6-180">-ResourceGroupName</span></span>
<span data-ttu-id="12ec6-181">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="12ec6-181">Resource Group Name</span></span>

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

### <span data-ttu-id="12ec6-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="12ec6-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="12ec6-183">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="12ec6-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="12ec6-184">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="12ec6-184">-WebApp</span></span>
<span data-ttu-id="12ec6-185">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="12ec6-185">WebApp Object</span></span>

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

### <span data-ttu-id="12ec6-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="12ec6-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="12ec6-187">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="12ec6-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="12ec6-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ec6-188">CommonParameters</span></span>
<span data-ttu-id="12ec6-189">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ec6-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ec6-190">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12ec6-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ec6-191">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12ec6-191">INPUTS</span></span>

### <span data-ttu-id="12ec6-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="12ec6-192">System.Int32</span></span>

### <span data-ttu-id="12ec6-193">System. String</span><span class="sxs-lookup"><span data-stu-id="12ec6-193">System.String</span></span>

### <span data-ttu-id="12ec6-194">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="12ec6-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="12ec6-195">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12ec6-195">OUTPUTS</span></span>

### <span data-ttu-id="12ec6-196">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="12ec6-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="12ec6-197">Notizen</span><span class="sxs-lookup"><span data-stu-id="12ec6-197">NOTES</span></span>
<span data-ttu-id="12ec6-198">Das unten angegebene Cmdlet hilft Ihnen, Azure Web App auf **DOTNETCORE** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="12ec6-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="12ec6-199">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-propertyobject $PropertiesObject-ResourceGroupName "Standard-Web-westus"-Microsoft. Web/Sites/config-Ressourcen "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="12ec6-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="12ec6-200">Ersetzen Sie die Werte von Default-Web-westus durch den Namen der Ressourcengruppe des Webanwendungs-und ContosoWebApp mit dem Namen der Webanwendung.</span><span class="sxs-lookup"><span data-stu-id="12ec6-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="12ec6-201">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12ec6-201">RELATED LINKS</span></span>

[<span data-ttu-id="12ec6-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="12ec6-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="12ec6-203">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="12ec6-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="12ec6-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="12ec6-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="12ec6-205">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="12ec6-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="12ec6-206">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="12ec6-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="12ec6-207">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="12ec6-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="12ec6-208">Neu – AzResource</span><span class="sxs-lookup"><span data-stu-id="12ec6-208">New-AzResource</span></span>](./New-AzResource.md)
