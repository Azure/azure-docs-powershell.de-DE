---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 2dc2356557a56ced2c0c09b70a1f6c2787438034
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827268"
---
# <span data-ttu-id="88dbe-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="88dbe-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="88dbe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="88dbe-103">Ändert einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="88dbe-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="88dbe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88dbe-104">SYNTAX</span></span>

### <span data-ttu-id="88dbe-105">S1</span><span class="sxs-lookup"><span data-stu-id="88dbe-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88dbe-106">S2</span><span class="sxs-lookup"><span data-stu-id="88dbe-106">S2</span></span>
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

## <span data-ttu-id="88dbe-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88dbe-107">DESCRIPTION</span></span>
<span data-ttu-id="88dbe-108">Das Cmdlet " **Set-AzWebApp** " legt einen Azure Web App-Steckplatz fest.</span><span class="sxs-lookup"><span data-stu-id="88dbe-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="88dbe-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88dbe-109">EXAMPLES</span></span>

### <span data-ttu-id="88dbe-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88dbe-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="88dbe-111">Mit diesem Befehl wird der Appservice-Plan geändert, der dem Slot001 zugeordnet ist, und zwar auf dem ContosoWebApp, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="88dbe-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="88dbe-112">Verwenden Sie den Link, um weitere Informationen zum Ändern des Appservice-Plans und der zugehörigen Einschränkungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88dbe-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="88dbe-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="88dbe-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="88dbe-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="88dbe-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="88dbe-115">Mit diesem Befehl wird HttpLoggingEnabled auf "true" festgelegt, wenn der Slot Slot001 in Bezug auf Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind-Web-westus</span><span class="sxs-lookup"><span data-stu-id="88dbe-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="88dbe-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="88dbe-116">PARAMETERS</span></span>

### <span data-ttu-id="88dbe-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="88dbe-117">-AppServicePlan</span></span>
<span data-ttu-id="88dbe-118">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="88dbe-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="88dbe-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="88dbe-119">-AppSettings</span></span>
<span data-ttu-id="88dbe-120">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="88dbe-120">App Settings HashTable.</span></span> <span data-ttu-id="88dbe-121">Vorhandene App-Einstellungen werden ersetzt, wobei alle nicht bereitgestellten Einstellungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="88dbe-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="88dbe-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88dbe-122">-AsJob</span></span>
<span data-ttu-id="88dbe-123">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="88dbe-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88dbe-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="88dbe-124">-AssignIdentity</span></span>
<span data-ttu-id="88dbe-125">Aktivieren/Deaktivieren von MSI für einen vorhandenen Steckplatz [Preview]</span><span class="sxs-lookup"><span data-stu-id="88dbe-125">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="88dbe-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="88dbe-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="88dbe-127">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="88dbe-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="88dbe-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="88dbe-128">-AzureStoragePath</span></span>
<span data-ttu-id="88dbe-129">Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="88dbe-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="88dbe-130">Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="88dbe-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="88dbe-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="88dbe-131">-ConnectionStrings</span></span>
<span data-ttu-id="88dbe-132">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="88dbe-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="88dbe-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="88dbe-133">-ContainerImageName</span></span>
<span data-ttu-id="88dbe-134">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="88dbe-134">Container Image Name</span></span>

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

### <span data-ttu-id="88dbe-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="88dbe-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="88dbe-136">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="88dbe-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="88dbe-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="88dbe-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="88dbe-138">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="88dbe-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="88dbe-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="88dbe-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="88dbe-140">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="88dbe-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="88dbe-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="88dbe-141">-DefaultDocuments</span></span>
<span data-ttu-id="88dbe-142">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="88dbe-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="88dbe-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88dbe-143">-DefaultProfile</span></span>
<span data-ttu-id="88dbe-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88dbe-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88dbe-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="88dbe-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="88dbe-146">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="88dbe-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="88dbe-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="88dbe-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="88dbe-148">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="88dbe-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="88dbe-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="88dbe-149">-HandlerMappings</span></span>
<span data-ttu-id="88dbe-150">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="88dbe-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="88dbe-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="88dbe-151">-HttpLoggingEnabled</span></span>
<span data-ttu-id="88dbe-152">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="88dbe-152">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="88dbe-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="88dbe-153">-HttpsOnly</span></span>
<span data-ttu-id="88dbe-154">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einem vorhandenen Steckplatz</span><span class="sxs-lookup"><span data-stu-id="88dbe-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="88dbe-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="88dbe-155">-ManagedPipelineMode</span></span>
<span data-ttu-id="88dbe-156">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="88dbe-156">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="88dbe-157">-Name</span><span class="sxs-lookup"><span data-stu-id="88dbe-157">-Name</span></span>
<span data-ttu-id="88dbe-158">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="88dbe-158">WebApp Name</span></span>

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

### <span data-ttu-id="88dbe-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="88dbe-159">-NetFrameworkVersion</span></span>
<span data-ttu-id="88dbe-160">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="88dbe-160">Net Framework Version</span></span>

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

### <span data-ttu-id="88dbe-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="88dbe-161">-NumberOfWorkers</span></span>
<span data-ttu-id="88dbe-162">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="88dbe-162">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="88dbe-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="88dbe-163">-PhpVersion</span></span>
<span data-ttu-id="88dbe-164">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="88dbe-164">Php Version</span></span>

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

### <span data-ttu-id="88dbe-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="88dbe-165">-RequestTracingEnabled</span></span>
<span data-ttu-id="88dbe-166">Anforderungs Ablaufverfolgung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="88dbe-166">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="88dbe-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88dbe-167">-ResourceGroupName</span></span>
<span data-ttu-id="88dbe-168">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="88dbe-168">Resource Group Name</span></span>

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

### <span data-ttu-id="88dbe-169">-Slot</span><span class="sxs-lookup"><span data-stu-id="88dbe-169">-Slot</span></span>
<span data-ttu-id="88dbe-170">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="88dbe-170">WebApp Slot Name</span></span>

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

### <span data-ttu-id="88dbe-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="88dbe-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="88dbe-172">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="88dbe-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="88dbe-173">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="88dbe-173">-WebApp</span></span>
<span data-ttu-id="88dbe-174">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="88dbe-174">WebApp Object</span></span>

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

### <span data-ttu-id="88dbe-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="88dbe-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="88dbe-176">Web Sockets enabled Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="88dbe-176">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="88dbe-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88dbe-177">CommonParameters</span></span>
<span data-ttu-id="88dbe-178">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88dbe-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88dbe-179">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88dbe-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88dbe-180">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88dbe-180">INPUTS</span></span>

### <span data-ttu-id="88dbe-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="88dbe-181">System.Int32</span></span>

### <span data-ttu-id="88dbe-182">System. String</span><span class="sxs-lookup"><span data-stu-id="88dbe-182">System.String</span></span>

### <span data-ttu-id="88dbe-183">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="88dbe-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="88dbe-184">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88dbe-184">OUTPUTS</span></span>

### <span data-ttu-id="88dbe-185">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="88dbe-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="88dbe-186">Notizen</span><span class="sxs-lookup"><span data-stu-id="88dbe-186">NOTES</span></span>

## <span data-ttu-id="88dbe-187">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88dbe-187">RELATED LINKS</span></span>

[<span data-ttu-id="88dbe-188">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="88dbe-188">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="88dbe-189">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="88dbe-189">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="88dbe-190">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="88dbe-190">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="88dbe-191">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="88dbe-191">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="88dbe-192">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="88dbe-192">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="88dbe-193">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="88dbe-193">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="88dbe-194">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="88dbe-194">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
