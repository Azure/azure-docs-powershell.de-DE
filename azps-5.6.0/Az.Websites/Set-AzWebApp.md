---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2f79abc7e5d6961c5e3f09deb843490d78c4614f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948171"
---
# <span data-ttu-id="c1c4d-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-101">Set-AzWebApp</span></span>

## <span data-ttu-id="c1c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c4d-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="c1c4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1c4d-104">SYNTAX</span></span>

### <span data-ttu-id="c1c4d-105">S1</span><span class="sxs-lookup"><span data-stu-id="c1c4d-105">S1</span></span>
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

### <span data-ttu-id="c1c4d-106">S2</span><span class="sxs-lookup"><span data-stu-id="c1c4d-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1c4d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1c4d-107">DESCRIPTION</span></span>
<span data-ttu-id="c1c4d-108">Das **Set-AzWebApp-Cmdlet** legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="c1c4d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1c4d-109">EXAMPLES</span></span>

### <span data-ttu-id="c1c4d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1c4d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="c1c4d-111">Mit diesem Befehl wird der Appserviceplan geändert, der der Web App ContosoWebApp zugeordnet ist, die der Ressourcengruppe Default-Web-WestUS zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c1c4d-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des Appserviceplans und der damit verbundenen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="c1c4d-113"> https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="c1c4d-113">https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="c1c4d-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c1c4d-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="c1c4d-115">Mit diesem Befehl wird HttpLoggingEnabled auf true für Web App ContosoWebApp festgelegt, die der Ressourcengruppe Default-Web-WestUS zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="c1c4d-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c1c4d-116">Example 3</span></span>

<span data-ttu-id="c1c4d-117">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="c1c4d-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="c1c4d-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="c1c4d-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="c1c4d-119">Example 4</span></span>

<span data-ttu-id="c1c4d-120">Im folgenden Beispiel wird eine Verbindungszeichenfolge mit dem Namen myConnectionString für Web App ContosoWebApp erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="c1c4d-121">Dadurch werden alle vorhandenen Verbindungszeichenfolgen für Web App ContosoWebApp ersetzt.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="c1c4d-122">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c1c4d-122">PARAMETERS</span></span>

### <span data-ttu-id="c1c4d-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="c1c4d-123">-AlwaysOn</span></span>
<span data-ttu-id="c1c4d-124">Stellen Sie sicher, dass die Web App immer geladen wird, statt nach dem Leerlauf zu entladen.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="c1c4d-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c1c4d-125">-AppServicePlan</span></span>
<span data-ttu-id="c1c4d-126">Name des App-Dienstplans</span><span class="sxs-lookup"><span data-stu-id="c1c4d-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="c1c4d-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c1c4d-127">-AppSettings</span></span>
<span data-ttu-id="c1c4d-128">HashTable "App-Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="c1c4d-128">App Settings HashTable.</span></span> <span data-ttu-id="c1c4d-129">Vorhandene App-Einstellungen werden ersetzt, und alle nicht bereitgestellten Einstellungen werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="c1c4d-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1c4d-130">-AsJob</span></span>
<span data-ttu-id="c1c4d-131">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c1c4d-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c1c4d-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c1c4d-132">-AssignIdentity</span></span>
<span data-ttu-id="c1c4d-133">Aktivieren/Deaktivieren von MSI in einer vorhandenen Azure WebApp oder FunctionApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c1c4d-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c1c4d-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="c1c4d-135">Name des Zielplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="c1c4d-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="c1c4d-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c1c4d-136">-AzureStoragePath</span></span>
<span data-ttu-id="c1c4d-137">Azure Storage zum Bereitstellen in einer Web App für Container.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="c1c4d-138">Verwenden New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="c1c4d-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="c1c4d-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c1c4d-139">-ConnectionStrings</span></span>
<span data-ttu-id="c1c4d-140">HashTable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="c1c4d-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="c1c4d-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c1c4d-141">-ContainerImageName</span></span>
<span data-ttu-id="c1c4d-142">Containerbildname</span><span class="sxs-lookup"><span data-stu-id="c1c4d-142">Container Image Name</span></span>

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

### <span data-ttu-id="c1c4d-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c1c4d-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c1c4d-144">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="c1c4d-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c1c4d-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c1c4d-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c1c4d-146">Url des privaten Containerregistrierungsservers</span><span class="sxs-lookup"><span data-stu-id="c1c4d-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c1c4d-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c1c4d-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="c1c4d-148">Benutzername für private Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="c1c4d-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c1c4d-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c1c4d-149">-DefaultDocuments</span></span>
<span data-ttu-id="c1c4d-150">Standarddokumentzeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="c1c4d-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="c1c4d-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c4d-151">-DefaultProfile</span></span>
<span data-ttu-id="c1c4d-152">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1c4d-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c1c4d-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c1c4d-154">Boolescher Detailfehlerprotokollierung aktiviert</span><span class="sxs-lookup"><span data-stu-id="c1c4d-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="c1c4d-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c1c4d-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c1c4d-156">Aktiviert/Deaktiviert die kontinuierliche Containerbereitstellung im Webhook</span><span class="sxs-lookup"><span data-stu-id="c1c4d-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c1c4d-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="c1c4d-157">-FtpsState</span></span>
<span data-ttu-id="c1c4d-158">Legen Sie den Wert für den Ftps-Zustand für eine App ein.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="c1c4d-159">Zulässige Werte [AllAllowed | Deaktivierte | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="c1c4d-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="c1c4d-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c1c4d-160">-HandlerMappings</span></span>
<span data-ttu-id="c1c4d-161">Handlerzuordnungen IList</span><span class="sxs-lookup"><span data-stu-id="c1c4d-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="c1c4d-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="c1c4d-162">-HostNames</span></span>
<span data-ttu-id="c1c4d-163">WebApp HostNames String Array</span><span class="sxs-lookup"><span data-stu-id="c1c4d-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="c1c4d-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c1c4d-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c1c4d-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c1c4d-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="c1c4d-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c1c4d-166">-HttpsOnly</span></span>
<span data-ttu-id="c1c4d-167">Aktivieren/Deaktivieren der Umleitung des datenverkehrs auf HTTPS in einer vorhandenen Azure WebApp oder FunctionApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c1c4d-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c1c4d-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="c1c4d-169">Name des verwalteten Pipelinemodus</span><span class="sxs-lookup"><span data-stu-id="c1c4d-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="c1c4d-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c1c4d-170">-MinTlsVersion</span></span>
<span data-ttu-id="c1c4d-171">Die für SSL-Anforderungen erforderliche Mindestversion von TLS.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="c1c4d-172">Zulässige Werte [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="c1c4d-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="c1c4d-173">-Name</span><span class="sxs-lookup"><span data-stu-id="c1c4d-173">-Name</span></span>
<span data-ttu-id="c1c4d-174">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="c1c4d-174">WebApp Name</span></span>

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

### <span data-ttu-id="c1c4d-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c1c4d-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="c1c4d-176">Net Framework Version</span><span class="sxs-lookup"><span data-stu-id="c1c4d-176">Net Framework Version</span></span>

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

### <span data-ttu-id="c1c4d-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c1c4d-177">-NumberOfWorkers</span></span>
<span data-ttu-id="c1c4d-178">Die Anzahl der zu zugeordneten Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="c1c4d-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="c1c4d-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c1c4d-179">-PhpVersion</span></span>
<span data-ttu-id="c1c4d-180">Php-Version</span><span class="sxs-lookup"><span data-stu-id="c1c4d-180">Php Version</span></span>

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

### <span data-ttu-id="c1c4d-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c1c4d-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="c1c4d-182">Anforderungsablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="c1c4d-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="c1c4d-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c4d-183">-ResourceGroupName</span></span>
<span data-ttu-id="c1c4d-184">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="c1c4d-184">Resource Group Name</span></span>

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

### <span data-ttu-id="c1c4d-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c1c4d-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c1c4d-186">Verwenden des booleschen 32-Bit-Workerprozesses</span><span class="sxs-lookup"><span data-stu-id="c1c4d-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="c1c4d-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-187">-WebApp</span></span>
<span data-ttu-id="c1c4d-188">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="c1c4d-188">WebApp Object</span></span>

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

### <span data-ttu-id="c1c4d-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c1c4d-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="c1c4d-190">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c1c4d-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="c1c4d-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c4d-191">CommonParameters</span></span>
<span data-ttu-id="c1c4d-192">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c4d-193">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1c4d-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c4d-194">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1c4d-194">INPUTS</span></span>

### <span data-ttu-id="c1c4d-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c1c4d-195">System.Int32</span></span>

### <span data-ttu-id="c1c4d-196">System.String</span><span class="sxs-lookup"><span data-stu-id="c1c4d-196">System.String</span></span>

### <span data-ttu-id="c1c4d-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c1c4d-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c1c4d-198">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1c4d-198">OUTPUTS</span></span>

### <span data-ttu-id="c1c4d-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c1c4d-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c1c4d-200">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c1c4d-200">NOTES</span></span>
<span data-ttu-id="c1c4d-201">Unten bereitgestelltes Cmdlet hilft Ihnen beim Aktualisieren von Azure Web App auf **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="c1c4d-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="c1c4d-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="c1c4d-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="c1c4d-203">Ersetzen Sie die Werte von Default-Web-WestUS durch den Ressourcengruppennamen der Webapp und ContosoWebApp durch den Webapp-Namen.</span><span class="sxs-lookup"><span data-stu-id="c1c4d-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="c1c4d-204">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c1c4d-204">RELATED LINKS</span></span>

[<span data-ttu-id="c1c4d-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c1c4d-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c1c4d-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c1c4d-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c1c4d-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c1c4d-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c1c4d-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="c1c4d-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="c1c4d-211">New-AzResource</span></span>](./New-AzResource.md)
