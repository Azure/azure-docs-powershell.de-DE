---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658499"
---
# <span data-ttu-id="08ff6-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ff6-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="08ff6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="08ff6-103">Ändert einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="08ff6-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="08ff6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08ff6-104">SYNTAX</span></span>

### <span data-ttu-id="08ff6-105">S1</span><span class="sxs-lookup"><span data-stu-id="08ff6-105">S1</span></span>
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

### <span data-ttu-id="08ff6-106">S2</span><span class="sxs-lookup"><span data-stu-id="08ff6-106">S2</span></span>
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

## <span data-ttu-id="08ff6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08ff6-107">DESCRIPTION</span></span>
<span data-ttu-id="08ff6-108">Das Cmdlet " **Set-AzWebApp** " legt einen Azure Web App-Steckplatz fest.</span><span class="sxs-lookup"><span data-stu-id="08ff6-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="08ff6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08ff6-109">EXAMPLES</span></span>

### <span data-ttu-id="08ff6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08ff6-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="08ff6-111">Mit diesem Befehl wird der Appservice-Plan geändert, der dem Slot001 zugeordnet ist, und zwar auf dem ContosoWebApp, das der Ressourcengruppe Default-Web-westus zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="08ff6-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="08ff6-112">Verwenden Sie den Link zu learm, um mehr über das Ändern des Appservice-Plans und die damit verbundenen Einschränkungen zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="08ff6-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="08ff6-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="08ff6-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="08ff6-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="08ff6-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="08ff6-115">Mit diesem Befehl wird HttpLoggingEnabled auf "true" festgelegt, wenn der Slot Slot001 in Bezug auf Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind-Web-westus</span><span class="sxs-lookup"><span data-stu-id="08ff6-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="08ff6-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="08ff6-116">PARAMETERS</span></span>

### <span data-ttu-id="08ff6-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="08ff6-117">-AppServicePlan</span></span>
<span data-ttu-id="08ff6-118">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="08ff6-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="08ff6-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="08ff6-119">-AppSettings</span></span>
<span data-ttu-id="08ff6-120">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="08ff6-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="08ff6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08ff6-121">-AsJob</span></span>
<span data-ttu-id="08ff6-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="08ff6-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08ff6-123">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="08ff6-123">-AssignIdentity</span></span>
<span data-ttu-id="08ff6-124">Aktivieren/Deaktivieren von MSI für einen vorhandenen Steckplatz [Preview]</span><span class="sxs-lookup"><span data-stu-id="08ff6-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="08ff6-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="08ff6-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="08ff6-126">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="08ff6-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="08ff6-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="08ff6-127">-AzureStoragePath</span></span>
<span data-ttu-id="08ff6-128">Azure-Speicher, der in einer Web-App für Container bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08ff6-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="08ff6-129">Verwenden von New-AzureRmWebAppAzureStoragePath zum Erstellen</span><span class="sxs-lookup"><span data-stu-id="08ff6-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="08ff6-130">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="08ff6-130">-ConnectionStrings</span></span>
<span data-ttu-id="08ff6-131">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="08ff6-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="08ff6-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="08ff6-132">-ContainerImageName</span></span>
<span data-ttu-id="08ff6-133">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="08ff6-133">Container Image Name</span></span>

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

### <span data-ttu-id="08ff6-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="08ff6-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="08ff6-135">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="08ff6-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="08ff6-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="08ff6-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="08ff6-137">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="08ff6-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="08ff6-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="08ff6-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="08ff6-139">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="08ff6-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="08ff6-140">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="08ff6-140">-DefaultDocuments</span></span>
<span data-ttu-id="08ff6-141">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="08ff6-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="08ff6-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08ff6-142">-DefaultProfile</span></span>
<span data-ttu-id="08ff6-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08ff6-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08ff6-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="08ff6-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="08ff6-145">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="08ff6-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="08ff6-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="08ff6-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="08ff6-147">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="08ff6-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="08ff6-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="08ff6-148">-HandlerMappings</span></span>
<span data-ttu-id="08ff6-149">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="08ff6-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="08ff6-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="08ff6-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="08ff6-151">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="08ff6-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="08ff6-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="08ff6-152">-HttpsOnly</span></span>
<span data-ttu-id="08ff6-153">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einem vorhandenen Steckplatz</span><span class="sxs-lookup"><span data-stu-id="08ff6-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="08ff6-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="08ff6-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="08ff6-155">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="08ff6-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="08ff6-156">-Name</span><span class="sxs-lookup"><span data-stu-id="08ff6-156">-Name</span></span>
<span data-ttu-id="08ff6-157">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="08ff6-157">WebApp Name</span></span>

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

### <span data-ttu-id="08ff6-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="08ff6-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="08ff6-159">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="08ff6-159">Net Framework Version</span></span>

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

### <span data-ttu-id="08ff6-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="08ff6-160">-NumberOfWorkers</span></span>
<span data-ttu-id="08ff6-161">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="08ff6-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="08ff6-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="08ff6-162">-PhpVersion</span></span>
<span data-ttu-id="08ff6-163">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="08ff6-163">Php Version</span></span>

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

### <span data-ttu-id="08ff6-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="08ff6-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="08ff6-165">Anforderungs Ablaufverfolgung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="08ff6-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="08ff6-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08ff6-166">-ResourceGroupName</span></span>
<span data-ttu-id="08ff6-167">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="08ff6-167">Resource Group Name</span></span>

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

### <span data-ttu-id="08ff6-168">-Slot</span><span class="sxs-lookup"><span data-stu-id="08ff6-168">-Slot</span></span>
<span data-ttu-id="08ff6-169">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="08ff6-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="08ff6-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="08ff6-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="08ff6-171">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="08ff6-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="08ff6-172">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="08ff6-172">-WebApp</span></span>
<span data-ttu-id="08ff6-173">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="08ff6-173">WebApp Object</span></span>

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

### <span data-ttu-id="08ff6-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="08ff6-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="08ff6-175">Web Sockets enabled Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="08ff6-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="08ff6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08ff6-176">CommonParameters</span></span>
<span data-ttu-id="08ff6-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08ff6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08ff6-178">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08ff6-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08ff6-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08ff6-179">INPUTS</span></span>

### <span data-ttu-id="08ff6-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="08ff6-180">System.Int32</span></span>

### <span data-ttu-id="08ff6-181">System. String</span><span class="sxs-lookup"><span data-stu-id="08ff6-181">System.String</span></span>

### <span data-ttu-id="08ff6-182">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="08ff6-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08ff6-183">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08ff6-183">OUTPUTS</span></span>

### <span data-ttu-id="08ff6-184">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="08ff6-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="08ff6-185">Notizen</span><span class="sxs-lookup"><span data-stu-id="08ff6-185">NOTES</span></span>

## <span data-ttu-id="08ff6-186">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08ff6-186">RELATED LINKS</span></span>

[<span data-ttu-id="08ff6-187">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ff6-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="08ff6-188">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ff6-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="08ff6-189">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ff6-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="08ff6-190">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ff6-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="08ff6-191">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ff6-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="08ff6-192">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="08ff6-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="08ff6-193">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="08ff6-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
