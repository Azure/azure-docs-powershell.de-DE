---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179343"
---
# <span data-ttu-id="0ed30-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ed30-101">Set-AzWebApp</span></span>

## <span data-ttu-id="0ed30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ed30-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed30-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0ed30-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="0ed30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ed30-104">SYNTAX</span></span>

### <span data-ttu-id="0ed30-105">S1</span><span class="sxs-lookup"><span data-stu-id="0ed30-105">S1</span></span>
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

### <span data-ttu-id="0ed30-106">S2</span><span class="sxs-lookup"><span data-stu-id="0ed30-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ed30-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ed30-107">DESCRIPTION</span></span>
<span data-ttu-id="0ed30-108">Das Cmdlet " **Set-AzWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="0ed30-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="0ed30-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ed30-109">EXAMPLES</span></span>

### <span data-ttu-id="0ed30-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0ed30-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="0ed30-111">Mit diesem Befehl wird der Appservice-Plan geändert, der dem Web-App-ContosoWebApp zugeordnet ist, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0ed30-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="0ed30-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des Appservice-Plans und der zugehörigen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ed30-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="0ed30-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="0ed30-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="0ed30-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0ed30-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="0ed30-115">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="0ed30-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="0ed30-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0ed30-116">Example 3</span></span>

<span data-ttu-id="0ed30-117">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0ed30-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="0ed30-118">automatisch</span><span class="sxs-lookup"><span data-stu-id="0ed30-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="0ed30-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="0ed30-119">Example 4</span></span>

<span data-ttu-id="0ed30-120">Im folgenden Beispiel wird eine Verbindungszeichenfolge mit dem Namen myConnection String für Web App ContosoWebApp erstellt.</span><span class="sxs-lookup"><span data-stu-id="0ed30-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="0ed30-121">Dadurch werden alle vorhandenen Verbindungszeichenfolgen für Web App ContosoWebApp ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0ed30-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="0ed30-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ed30-122">PARAMETERS</span></span>

### <span data-ttu-id="0ed30-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="0ed30-123">-AlwaysOn</span></span>
<span data-ttu-id="0ed30-124">Stellen Sie sicher, dass die Web-App immer geladen wird, nachdem Sie inaktiv war.</span><span class="sxs-lookup"><span data-stu-id="0ed30-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="0ed30-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0ed30-125">-AppServicePlan</span></span>
<span data-ttu-id="0ed30-126">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="0ed30-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="0ed30-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="0ed30-127">-AppSettings</span></span>
<span data-ttu-id="0ed30-128">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0ed30-128">App Settings HashTable.</span></span> <span data-ttu-id="0ed30-129">Vorhandene App-Einstellungen werden ersetzt, wobei alle nicht bereitgestellten Einstellungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="0ed30-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="0ed30-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ed30-130">-AsJob</span></span>
<span data-ttu-id="0ed30-131">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0ed30-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ed30-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0ed30-132">-AssignIdentity</span></span>
<span data-ttu-id="0ed30-133">Aktivieren/Deaktivieren von MSI für eine vorhandene Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="0ed30-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="0ed30-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="0ed30-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="0ed30-135">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="0ed30-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="0ed30-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="0ed30-136">-AzureStoragePath</span></span>
<span data-ttu-id="0ed30-137">Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ed30-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="0ed30-138">Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="0ed30-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="0ed30-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="0ed30-139">-ConnectionStrings</span></span>
<span data-ttu-id="0ed30-140">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="0ed30-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="0ed30-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="0ed30-141">-ContainerImageName</span></span>
<span data-ttu-id="0ed30-142">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="0ed30-142">Container Image Name</span></span>

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

### <span data-ttu-id="0ed30-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="0ed30-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="0ed30-144">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="0ed30-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="0ed30-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="0ed30-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="0ed30-146">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="0ed30-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="0ed30-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="0ed30-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="0ed30-148">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="0ed30-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="0ed30-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="0ed30-149">-DefaultDocuments</span></span>
<span data-ttu-id="0ed30-150">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="0ed30-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="0ed30-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed30-151">-DefaultProfile</span></span>
<span data-ttu-id="0ed30-152">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ed30-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ed30-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ed30-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="0ed30-154">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0ed30-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="0ed30-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="0ed30-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="0ed30-156">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="0ed30-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="0ed30-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="0ed30-157">-FtpsState</span></span>
<span data-ttu-id="0ed30-158">Setzen Sie den Wert für den Zustand "FTP" für eine APP.</span><span class="sxs-lookup"><span data-stu-id="0ed30-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="0ed30-159">Zulässige Werte [alle erlaubt | Deaktiviert | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="0ed30-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="0ed30-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="0ed30-160">-HandlerMappings</span></span>
<span data-ttu-id="0ed30-161">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="0ed30-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="0ed30-162">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="0ed30-162">-HostNames</span></span>
<span data-ttu-id="0ed30-163">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="0ed30-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="0ed30-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ed30-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="0ed30-165">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0ed30-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="0ed30-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0ed30-166">-HttpsOnly</span></span>
<span data-ttu-id="0ed30-167">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einer vorhandenen Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="0ed30-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="0ed30-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="0ed30-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="0ed30-169">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="0ed30-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="0ed30-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0ed30-170">-MinTlsVersion</span></span>
<span data-ttu-id="0ed30-171">Die für SSL-Anforderungen erforderliche minimale Version von TLS.</span><span class="sxs-lookup"><span data-stu-id="0ed30-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="0ed30-172">Zulässige Werte [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="0ed30-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="0ed30-173">-Name</span><span class="sxs-lookup"><span data-stu-id="0ed30-173">-Name</span></span>
<span data-ttu-id="0ed30-174">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0ed30-174">WebApp Name</span></span>

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

### <span data-ttu-id="0ed30-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="0ed30-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="0ed30-176">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="0ed30-176">Net Framework Version</span></span>

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

### <span data-ttu-id="0ed30-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="0ed30-177">-NumberOfWorkers</span></span>
<span data-ttu-id="0ed30-178">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="0ed30-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="0ed30-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="0ed30-179">-PhpVersion</span></span>
<span data-ttu-id="0ed30-180">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="0ed30-180">Php Version</span></span>

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

### <span data-ttu-id="0ed30-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="0ed30-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="0ed30-182">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="0ed30-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="0ed30-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed30-183">-ResourceGroupName</span></span>
<span data-ttu-id="0ed30-184">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0ed30-184">Resource Group Name</span></span>

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

### <span data-ttu-id="0ed30-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="0ed30-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="0ed30-186">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="0ed30-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="0ed30-187">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="0ed30-187">-WebApp</span></span>
<span data-ttu-id="0ed30-188">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="0ed30-188">WebApp Object</span></span>

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

### <span data-ttu-id="0ed30-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="0ed30-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="0ed30-190">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0ed30-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="0ed30-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed30-191">CommonParameters</span></span>
<span data-ttu-id="0ed30-192">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ed30-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed30-193">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ed30-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed30-194">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ed30-194">INPUTS</span></span>

### <span data-ttu-id="0ed30-195">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0ed30-195">System.Int32</span></span>

### <span data-ttu-id="0ed30-196">System. String</span><span class="sxs-lookup"><span data-stu-id="0ed30-196">System.String</span></span>

### <span data-ttu-id="0ed30-197">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0ed30-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0ed30-198">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ed30-198">OUTPUTS</span></span>

### <span data-ttu-id="0ed30-199">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0ed30-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0ed30-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ed30-200">NOTES</span></span>
<span data-ttu-id="0ed30-201">Das unten angegebene Cmdlet hilft Ihnen, Azure Web App auf **DOTNETCORE** zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0ed30-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="0ed30-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-propertyobject $PropertiesObject-ResourceGroupName "Standard-Web-westus"-Microsoft. Web/Sites/config-Ressourcen "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="0ed30-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="0ed30-203">Ersetzen Sie die Werte von Default-Web-westus durch den Namen der Ressourcengruppe des Webanwendungs-und ContosoWebApp mit dem Namen der Webanwendung.</span><span class="sxs-lookup"><span data-stu-id="0ed30-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="0ed30-204">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ed30-204">RELATED LINKS</span></span>

[<span data-ttu-id="0ed30-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ed30-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0ed30-206">Neu – AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ed30-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0ed30-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ed30-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0ed30-208">Neustart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ed30-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0ed30-209">Anfang-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ed30-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="0ed30-210">Stopp-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0ed30-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="0ed30-211">Neu – AzResource</span><span class="sxs-lookup"><span data-stu-id="0ed30-211">New-AzResource</span></span>](./New-AzResource.md)
