---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d07d85aa9747982f223d45c40fc8897a0b0e3e73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948168"
---
# <span data-ttu-id="95591-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95591-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="95591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95591-102">SYNOPSIS</span></span>
<span data-ttu-id="95591-103">Ändert einen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="95591-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="95591-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95591-104">SYNTAX</span></span>

### <span data-ttu-id="95591-105">S1</span><span class="sxs-lookup"><span data-stu-id="95591-105">S1</span></span>
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

### <span data-ttu-id="95591-106">S2</span><span class="sxs-lookup"><span data-stu-id="95591-106">S2</span></span>
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

## <span data-ttu-id="95591-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95591-107">DESCRIPTION</span></span>
<span data-ttu-id="95591-108">Das **Set-AzWebApp-Cmdlet** legt einen Azure Web App-Slot fest.</span><span class="sxs-lookup"><span data-stu-id="95591-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="95591-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95591-109">EXAMPLES</span></span>

### <span data-ttu-id="95591-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95591-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="95591-111">Mit diesem Befehl wird der dem Slot001 zugeordnete Appserviceplan in der Webapp ContosoWebApp geändert, die der Ressourcengruppe Default-Web-WestUS zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="95591-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="95591-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des Appserviceplans und der damit verbundenen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="95591-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="95591-113"> https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="95591-113">https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="95591-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="95591-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="95591-115">Mit diesem Befehl wird HttpLoggingEnabled für Slot Slot001 im Zusammenhang mit Web App ContosoWebApp, die der Ressourcengruppe Default-Web-WestUS zugeordnet ist, auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="95591-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="95591-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="95591-116">Example 3</span></span>

<span data-ttu-id="95591-117">Ändert einen Azure Web App-Slot.</span><span class="sxs-lookup"><span data-stu-id="95591-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="95591-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="95591-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="95591-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="95591-119">PARAMETERS</span></span>

### <span data-ttu-id="95591-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="95591-120">-AlwaysOn</span></span>
<span data-ttu-id="95591-121">Stellen Sie sicher, dass die Web App immer geladen wird, statt nach dem Leerlauf zu entladen.</span><span class="sxs-lookup"><span data-stu-id="95591-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="95591-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95591-122">-AppServicePlan</span></span>
<span data-ttu-id="95591-123">Name des App-Dienstplans</span><span class="sxs-lookup"><span data-stu-id="95591-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="95591-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="95591-124">-AppSettings</span></span>
<span data-ttu-id="95591-125">HashTable "App-Einstellungen".</span><span class="sxs-lookup"><span data-stu-id="95591-125">App Settings HashTable.</span></span> <span data-ttu-id="95591-126">Vorhandene App-Einstellungen werden ersetzt, und alle nicht bereitgestellten Einstellungen werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="95591-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="95591-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95591-127">-AsJob</span></span>
<span data-ttu-id="95591-128">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="95591-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95591-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="95591-129">-AssignIdentity</span></span>
<span data-ttu-id="95591-130">Aktivieren/Deaktivieren von MSI an einem vorhandenen Slot [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="95591-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="95591-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="95591-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="95591-132">Name des Zielplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="95591-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="95591-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="95591-133">-AzureStoragePath</span></span>
<span data-ttu-id="95591-134">Azure Storage zum Bereitstellen in einer Web App für Container.</span><span class="sxs-lookup"><span data-stu-id="95591-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="95591-135">Verwenden New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="95591-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="95591-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="95591-136">-ConnectionStrings</span></span>
<span data-ttu-id="95591-137">HashTable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="95591-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="95591-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="95591-138">-ContainerImageName</span></span>
<span data-ttu-id="95591-139">Containerbildname</span><span class="sxs-lookup"><span data-stu-id="95591-139">Container Image Name</span></span>

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

### <span data-ttu-id="95591-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="95591-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="95591-141">Private Container Registry Password</span><span class="sxs-lookup"><span data-stu-id="95591-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="95591-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="95591-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="95591-143">Url des privaten Containerregistrierungsservers</span><span class="sxs-lookup"><span data-stu-id="95591-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="95591-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="95591-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="95591-145">Benutzername für private Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="95591-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="95591-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="95591-146">-DefaultDocuments</span></span>
<span data-ttu-id="95591-147">Standarddokumentzeichenfolgenarray</span><span class="sxs-lookup"><span data-stu-id="95591-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="95591-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95591-148">-DefaultProfile</span></span>
<span data-ttu-id="95591-149">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95591-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95591-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="95591-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="95591-151">Boolescher Detailfehlerprotokollierung aktiviert</span><span class="sxs-lookup"><span data-stu-id="95591-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="95591-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="95591-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="95591-153">Aktiviert/Deaktiviert die kontinuierliche Containerbereitstellung im Webhook</span><span class="sxs-lookup"><span data-stu-id="95591-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="95591-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="95591-154">-FtpsState</span></span>
<span data-ttu-id="95591-155">Legen Sie den Wert für den Ftps-Zustand für eine App ein.</span><span class="sxs-lookup"><span data-stu-id="95591-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="95591-156">Zulässige Werte [AllAllowed | Deaktivierte | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="95591-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="95591-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="95591-157">-HandlerMappings</span></span>
<span data-ttu-id="95591-158">Handlerzuordnungen IList</span><span class="sxs-lookup"><span data-stu-id="95591-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="95591-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="95591-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="95591-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="95591-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="95591-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="95591-161">-HttpsOnly</span></span>
<span data-ttu-id="95591-162">Aktivieren/Deaktivieren der Umleitung des Datenverkehrs an HTTPS in einem vorhandenen Slot</span><span class="sxs-lookup"><span data-stu-id="95591-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="95591-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="95591-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="95591-164">Name des verwalteten Pipelinemodus</span><span class="sxs-lookup"><span data-stu-id="95591-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="95591-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="95591-165">-MinTlsVersion</span></span>
<span data-ttu-id="95591-166">Die für SSL-Anforderungen erforderliche Mindestversion von TLS.</span><span class="sxs-lookup"><span data-stu-id="95591-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="95591-167">Zulässige Werte [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="95591-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="95591-168">-Name</span><span class="sxs-lookup"><span data-stu-id="95591-168">-Name</span></span>
<span data-ttu-id="95591-169">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="95591-169">WebApp Name</span></span>

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

### <span data-ttu-id="95591-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="95591-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="95591-171">Net Framework Version</span><span class="sxs-lookup"><span data-stu-id="95591-171">Net Framework Version</span></span>

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

### <span data-ttu-id="95591-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="95591-172">-NumberOfWorkers</span></span>
<span data-ttu-id="95591-173">Die Anzahl der zu zugeordneten Arbeitskräfte</span><span class="sxs-lookup"><span data-stu-id="95591-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="95591-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="95591-174">-PhpVersion</span></span>
<span data-ttu-id="95591-175">Php-Version</span><span class="sxs-lookup"><span data-stu-id="95591-175">Php Version</span></span>

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

### <span data-ttu-id="95591-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="95591-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="95591-177">Boolescher Typ "Ablaufverfolgung anfordern"</span><span class="sxs-lookup"><span data-stu-id="95591-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="95591-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95591-178">-ResourceGroupName</span></span>
<span data-ttu-id="95591-179">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="95591-179">Resource Group Name</span></span>

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

### <span data-ttu-id="95591-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="95591-180">-Slot</span></span>
<span data-ttu-id="95591-181">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="95591-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="95591-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="95591-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="95591-183">Verwenden des booleschen 32-Bit-Workerprozesses</span><span class="sxs-lookup"><span data-stu-id="95591-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="95591-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="95591-184">-WebApp</span></span>
<span data-ttu-id="95591-185">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="95591-185">WebApp Object</span></span>

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

### <span data-ttu-id="95591-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="95591-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="95591-187">Boolesch aktivierte Websockets</span><span class="sxs-lookup"><span data-stu-id="95591-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="95591-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95591-188">CommonParameters</span></span>
<span data-ttu-id="95591-189">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95591-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95591-190">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95591-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95591-191">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95591-191">INPUTS</span></span>

### <span data-ttu-id="95591-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="95591-192">System.Int32</span></span>

### <span data-ttu-id="95591-193">System.String</span><span class="sxs-lookup"><span data-stu-id="95591-193">System.String</span></span>

### <span data-ttu-id="95591-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="95591-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="95591-195">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95591-195">OUTPUTS</span></span>

### <span data-ttu-id="95591-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="95591-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="95591-197">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="95591-197">NOTES</span></span>

## <span data-ttu-id="95591-198">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="95591-198">RELATED LINKS</span></span>

[<span data-ttu-id="95591-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95591-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="95591-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95591-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="95591-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95591-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="95591-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95591-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="95591-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95591-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="95591-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="95591-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="95591-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95591-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
