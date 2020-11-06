---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497138"
---
# <span data-ttu-id="e7e58-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7e58-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="e7e58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7e58-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e58-103">Ändert einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="e7e58-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7e58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7e58-104">SYNTAX</span></span>

### <span data-ttu-id="e7e58-105">S1</span><span class="sxs-lookup"><span data-stu-id="e7e58-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7e58-106">S2</span><span class="sxs-lookup"><span data-stu-id="e7e58-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e58-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7e58-107">DESCRIPTION</span></span>
<span data-ttu-id="e7e58-108">Das Cmdlet " **Set-AzureRmWebApp** " legt einen Azure Web App-Steckplatz fest.</span><span class="sxs-lookup"><span data-stu-id="e7e58-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="e7e58-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7e58-109">EXAMPLES</span></span>

### <span data-ttu-id="e7e58-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7e58-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="e7e58-111">Mit diesem Befehl wird HttpLoggingEnabled auf "true" festgelegt, wenn der Slot Slot001 in Bezug auf Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind-Web-westus</span><span class="sxs-lookup"><span data-stu-id="e7e58-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e7e58-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7e58-112">PARAMETERS</span></span>

### <span data-ttu-id="e7e58-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e7e58-113">-AppServicePlan</span></span>
<span data-ttu-id="e7e58-114">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="e7e58-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="e7e58-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="e7e58-115">-AppSettings</span></span>
<span data-ttu-id="e7e58-116">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e7e58-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="e7e58-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7e58-117">-AsJob</span></span>
<span data-ttu-id="e7e58-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e7e58-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7e58-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e7e58-119">-AssignIdentity</span></span>
<span data-ttu-id="e7e58-120">Aktivieren/Deaktivieren von MSI für einen vorhandenen Steckplatz [Preview]</span><span class="sxs-lookup"><span data-stu-id="e7e58-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="e7e58-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="e7e58-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="e7e58-122">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="e7e58-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="e7e58-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="e7e58-123">-ConnectionStrings</span></span>
<span data-ttu-id="e7e58-124">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="e7e58-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="e7e58-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="e7e58-125">-ContainerImageName</span></span>
<span data-ttu-id="e7e58-126">Name des Container Bilds</span><span class="sxs-lookup"><span data-stu-id="e7e58-126">Container Image Name</span></span>

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

### <span data-ttu-id="e7e58-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="e7e58-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="e7e58-128">Registrierungskennwort für private Container</span><span class="sxs-lookup"><span data-stu-id="e7e58-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="e7e58-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="e7e58-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="e7e58-130">URL des Registrierungsservers für private Container</span><span class="sxs-lookup"><span data-stu-id="e7e58-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="e7e58-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="e7e58-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="e7e58-132">Benutzername für private Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="e7e58-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="e7e58-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="e7e58-133">-DefaultDocuments</span></span>
<span data-ttu-id="e7e58-134">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="e7e58-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="e7e58-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e58-135">-DefaultProfile</span></span>
<span data-ttu-id="e7e58-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7e58-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e58-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e7e58-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="e7e58-138">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="e7e58-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="e7e58-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="e7e58-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="e7e58-140">Aktiviert/deaktiviert die Container-fortlaufende Bereitstellung webhook</span><span class="sxs-lookup"><span data-stu-id="e7e58-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="e7e58-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="e7e58-141">-HandlerMappings</span></span>
<span data-ttu-id="e7e58-142">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="e7e58-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="e7e58-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e7e58-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="e7e58-144">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="e7e58-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="e7e58-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e7e58-145">-HttpsOnly</span></span>
<span data-ttu-id="e7e58-146">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einem vorhandenen Steckplatz</span><span class="sxs-lookup"><span data-stu-id="e7e58-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="e7e58-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="e7e58-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="e7e58-148">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="e7e58-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="e7e58-149">-Name</span><span class="sxs-lookup"><span data-stu-id="e7e58-149">-Name</span></span>
<span data-ttu-id="e7e58-150">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="e7e58-150">WebApp Name</span></span>

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

### <span data-ttu-id="e7e58-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="e7e58-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="e7e58-152">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="e7e58-152">Net Framework Version</span></span>

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

### <span data-ttu-id="e7e58-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="e7e58-153">-NumberOfWorkers</span></span>
<span data-ttu-id="e7e58-154">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="e7e58-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="e7e58-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="e7e58-155">-PhpVersion</span></span>
<span data-ttu-id="e7e58-156">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="e7e58-156">Php Version</span></span>

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

### <span data-ttu-id="e7e58-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="e7e58-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="e7e58-158">Anforderungs Ablaufverfolgung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="e7e58-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="e7e58-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e58-159">-ResourceGroupName</span></span>
<span data-ttu-id="e7e58-160">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e7e58-160">Resource Group Name</span></span>

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

### <span data-ttu-id="e7e58-161">-Slot</span><span class="sxs-lookup"><span data-stu-id="e7e58-161">-Slot</span></span>
<span data-ttu-id="e7e58-162">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="e7e58-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="e7e58-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="e7e58-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="e7e58-164">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="e7e58-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="e7e58-165">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="e7e58-165">-WebApp</span></span>
<span data-ttu-id="e7e58-166">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="e7e58-166">WebApp Object</span></span>

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

### <span data-ttu-id="e7e58-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e7e58-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="e7e58-168">Web Sockets enabled Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="e7e58-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="e7e58-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e58-169">CommonParameters</span></span>
<span data-ttu-id="e7e58-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e58-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e58-171">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7e58-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e58-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7e58-172">INPUTS</span></span>

### <span data-ttu-id="e7e58-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e7e58-173">System.Int32</span></span>
<span data-ttu-id="e7e58-174">Parameter: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e7e58-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="e7e58-175">System. String</span><span class="sxs-lookup"><span data-stu-id="e7e58-175">System.String</span></span>

### <span data-ttu-id="e7e58-176">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="e7e58-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="e7e58-177">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="e7e58-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="e7e58-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7e58-178">OUTPUTS</span></span>

### <span data-ttu-id="e7e58-179">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="e7e58-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="e7e58-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7e58-180">NOTES</span></span>

## <span data-ttu-id="e7e58-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7e58-181">RELATED LINKS</span></span>

[<span data-ttu-id="e7e58-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7e58-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7e58-183">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7e58-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7e58-184">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7e58-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7e58-185">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7e58-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7e58-186">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7e58-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7e58-187">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e7e58-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="e7e58-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e7e58-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
