---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 5594e43b2e6c67e9df5b526f753557edd8a4d5ea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414729"
---
# <span data-ttu-id="cd92e-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-101">Set-AzWebApp</span></span>

## <span data-ttu-id="cd92e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd92e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd92e-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="cd92e-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="cd92e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd92e-104">SYNTAX</span></span>

### <span data-ttu-id="cd92e-105">S1</span><span class="sxs-lookup"><span data-stu-id="cd92e-105">S1</span></span>
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

### <span data-ttu-id="cd92e-106">S2</span><span class="sxs-lookup"><span data-stu-id="cd92e-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd92e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd92e-107">DESCRIPTION</span></span>
<span data-ttu-id="cd92e-108">Das **Cmdlet "Set-AzWebApp"** legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="cd92e-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="cd92e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd92e-109">EXAMPLES</span></span>

### <span data-ttu-id="cd92e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cd92e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="cd92e-111">Mit diesem Befehl wird der Appserviceplan geändert, der der Web App ContosoWebApp zugeordnet ist, die der Ressourcengruppe "Default-Web-WestUS" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cd92e-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="cd92e-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des zugehörigen Dienstplans und der damit verbundenen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cd92e-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="cd92e-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="cd92e-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="cd92e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cd92e-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="cd92e-115">Mit diesem Befehl wird "HttpLoggingEnabled" für die Web App "ContosoWebApp" auf "true" festgelegt, die der Ressourcengruppe "Default-Web-WestUS" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cd92e-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="cd92e-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="cd92e-116">Example 3</span></span>

<span data-ttu-id="cd92e-117">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="cd92e-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="cd92e-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="cd92e-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="cd92e-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="cd92e-119">Example 4</span></span>

<span data-ttu-id="cd92e-120">Im folgenden Beispiel wird eine Verbindungszeichenfolge namens "myConnectionString" für "Web App ContosoWebApp" erstellt.</span><span class="sxs-lookup"><span data-stu-id="cd92e-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="cd92e-121">Dadurch werden alle vorhandenen Verbindungszeichenfolgen für die Web App ContosoWebApp ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cd92e-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="cd92e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd92e-122">PARAMETERS</span></span>

### <span data-ttu-id="cd92e-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="cd92e-123">-AlwaysOn</span></span>
<span data-ttu-id="cd92e-124">Stellen Sie sicher, dass die Web App die ganze Zeit geladen wird, anstatt sie nach dem Leerlauf zu entladen.</span><span class="sxs-lookup"><span data-stu-id="cd92e-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="cd92e-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="cd92e-125">-AppServicePlan</span></span>
<span data-ttu-id="cd92e-126">Name des App-Serviceplans</span><span class="sxs-lookup"><span data-stu-id="cd92e-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="cd92e-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="cd92e-127">-AppSettings</span></span>
<span data-ttu-id="cd92e-128">HashTable "App-Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="cd92e-128">App Settings HashTable.</span></span> <span data-ttu-id="cd92e-129">Vorhandene Einstellungen der App werden ersetzt, und alle nicht bereitgestellten Einstellungen werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="cd92e-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="cd92e-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd92e-130">-AsJob</span></span>
<span data-ttu-id="cd92e-131">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cd92e-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd92e-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="cd92e-132">-AssignIdentity</span></span>
<span data-ttu-id="cd92e-133">Aktivieren/Deaktivieren von MSI in einer vorhandenen Azure WebApp oder FunctionApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="cd92e-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="cd92e-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="cd92e-135">Name des Zielplatzes für automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="cd92e-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="cd92e-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="cd92e-136">-AzureStoragePath</span></span>
<span data-ttu-id="cd92e-137">Azure Storage zum Bereitstellen in einer Web App für Container.</span><span class="sxs-lookup"><span data-stu-id="cd92e-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="cd92e-138">Verwenden New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="cd92e-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="cd92e-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="cd92e-139">-ConnectionStrings</span></span>
<span data-ttu-id="cd92e-140">HashTable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="cd92e-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="cd92e-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="cd92e-141">-ContainerImageName</span></span>
<span data-ttu-id="cd92e-142">Container Image Name</span><span class="sxs-lookup"><span data-stu-id="cd92e-142">Container Image Name</span></span>

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

### <span data-ttu-id="cd92e-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="cd92e-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="cd92e-144">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="cd92e-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="cd92e-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="cd92e-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="cd92e-146">URL des Registrierungsservers für privaten Container</span><span class="sxs-lookup"><span data-stu-id="cd92e-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="cd92e-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="cd92e-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="cd92e-148">Private Container Registry Username</span><span class="sxs-lookup"><span data-stu-id="cd92e-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="cd92e-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="cd92e-149">-DefaultDocuments</span></span>
<span data-ttu-id="cd92e-150">Standarddokumentzeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="cd92e-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="cd92e-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd92e-151">-DefaultProfile</span></span>
<span data-ttu-id="cd92e-152">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd92e-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd92e-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="cd92e-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="cd92e-154">Boolescher Wert für die detaillierte Fehlerprotokollierung</span><span class="sxs-lookup"><span data-stu-id="cd92e-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="cd92e-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="cd92e-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="cd92e-156">Aktiviert/Deaktiviert den Container-Webhook für die fortlaufende Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="cd92e-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="cd92e-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="cd92e-157">-FtpsState</span></span>
<span data-ttu-id="cd92e-158">Legen Sie den Wert für den Ftps-Zustand für eine App ein.</span><span class="sxs-lookup"><span data-stu-id="cd92e-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="cd92e-159">Zulässige Werte [AllAllowed | Deaktivierte | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="cd92e-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="cd92e-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="cd92e-160">-HandlerMappings</span></span>
<span data-ttu-id="cd92e-161">Handlerzuordnungen IList</span><span class="sxs-lookup"><span data-stu-id="cd92e-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="cd92e-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="cd92e-162">-HostNames</span></span>
<span data-ttu-id="cd92e-163">WebApp HostNames String Array</span><span class="sxs-lookup"><span data-stu-id="cd92e-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="cd92e-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="cd92e-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="cd92e-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="cd92e-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="cd92e-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="cd92e-166">-HttpsOnly</span></span>
<span data-ttu-id="cd92e-167">Aktivieren/Deaktivieren der Umleitung des ganzen Datenverkehrs an HTTPS in einer vorhandenen Azure WebApp oder FunctionApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="cd92e-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="cd92e-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="cd92e-169">Name des verwalteten Pipelinemodus</span><span class="sxs-lookup"><span data-stu-id="cd92e-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="cd92e-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="cd92e-170">-MinTlsVersion</span></span>
<span data-ttu-id="cd92e-171">Die für DIE SSL-Anforderungen mindestens erforderliche Version von TLS.</span><span class="sxs-lookup"><span data-stu-id="cd92e-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="cd92e-172">Zulässige Werte [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="cd92e-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="cd92e-173">-Name</span><span class="sxs-lookup"><span data-stu-id="cd92e-173">-Name</span></span>
<span data-ttu-id="cd92e-174">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="cd92e-174">WebApp Name</span></span>

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

### <span data-ttu-id="cd92e-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="cd92e-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="cd92e-176">Net Framework Version</span><span class="sxs-lookup"><span data-stu-id="cd92e-176">Net Framework Version</span></span>

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

### <span data-ttu-id="cd92e-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="cd92e-177">-NumberOfWorkers</span></span>
<span data-ttu-id="cd92e-178">Die Anzahl der zu zugeordneten Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="cd92e-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="cd92e-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="cd92e-179">-PhpVersion</span></span>
<span data-ttu-id="cd92e-180">Php-Version</span><span class="sxs-lookup"><span data-stu-id="cd92e-180">Php Version</span></span>

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

### <span data-ttu-id="cd92e-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="cd92e-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="cd92e-182">Anforderungsablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="cd92e-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="cd92e-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd92e-183">-ResourceGroupName</span></span>
<span data-ttu-id="cd92e-184">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="cd92e-184">Resource Group Name</span></span>

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

### <span data-ttu-id="cd92e-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="cd92e-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="cd92e-186">Verwenden des booleschen 32-Bit-Workerprozesses</span><span class="sxs-lookup"><span data-stu-id="cd92e-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="cd92e-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-187">-WebApp</span></span>
<span data-ttu-id="cd92e-188">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="cd92e-188">WebApp Object</span></span>

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

### <span data-ttu-id="cd92e-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="cd92e-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="cd92e-190">Boolescher Wert von WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="cd92e-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="cd92e-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd92e-191">CommonParameters</span></span>
<span data-ttu-id="cd92e-192">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd92e-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd92e-193">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd92e-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd92e-194">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd92e-194">INPUTS</span></span>

### <span data-ttu-id="cd92e-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="cd92e-195">System.Int32</span></span>

### <span data-ttu-id="cd92e-196">System.String</span><span class="sxs-lookup"><span data-stu-id="cd92e-196">System.String</span></span>

### <span data-ttu-id="cd92e-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="cd92e-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cd92e-198">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd92e-198">OUTPUTS</span></span>

### <span data-ttu-id="cd92e-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="cd92e-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cd92e-200">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cd92e-200">NOTES</span></span>
<span data-ttu-id="cd92e-201">Das unten bereitgestellte Cmdlet hilft Ihnen beim Aktualisieren von Azure Web App auf **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="cd92e-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="cd92e-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="cd92e-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="cd92e-203">Ersetzen Sie die Werte von "Default-Web-WestUS" durch den Ressourcengruppennamen "webapp" und "ContosoWebApp" durch den Webapp-Namen.</span><span class="sxs-lookup"><span data-stu-id="cd92e-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="cd92e-204">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cd92e-204">RELATED LINKS</span></span>

[<span data-ttu-id="cd92e-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="cd92e-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="cd92e-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="cd92e-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="cd92e-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="cd92e-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cd92e-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

