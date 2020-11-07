---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 245ce5ab011f03b8d8331b5d80fa4eeb01e19e15
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850183"
---
# <span data-ttu-id="e6cd3-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e6cd3-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="e6cd3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cd3-103">Ändert einen Azure Web App-Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="e6cd3-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6cd3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6cd3-104">SYNTAX</span></span>

### <span data-ttu-id="e6cd3-105">S1</span><span class="sxs-lookup"><span data-stu-id="e6cd3-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6cd3-106">S2</span><span class="sxs-lookup"><span data-stu-id="e6cd3-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6cd3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6cd3-107">DESCRIPTION</span></span>
<span data-ttu-id="e6cd3-108">Das Cmdlet " **Set-AzureRmWebApp** " legt einen Azure Web App-Steckplatz fest.</span><span class="sxs-lookup"><span data-stu-id="e6cd3-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="e6cd3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="e6cd3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6cd3-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="e6cd3-111">Mit diesem Befehl wird HttpLoggingEnabled auf "true" festgelegt, wenn der Slot Slot001 in Bezug auf Web-App-ContosoWebApp, die mit der Ressourcengruppe Standard verknüpft sind-Web-westus</span><span class="sxs-lookup"><span data-stu-id="e6cd3-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="e6cd3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6cd3-112">PARAMETERS</span></span>

### <span data-ttu-id="e6cd3-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e6cd3-113">-AppServicePlan</span></span>
<span data-ttu-id="e6cd3-114">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="e6cd3-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="e6cd3-115">-AppSettings</span></span>
<span data-ttu-id="e6cd3-116">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e6cd3-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="e6cd3-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="e6cd3-118">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="e6cd3-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="e6cd3-119">-ConnectionStrings</span></span>
<span data-ttu-id="e6cd3-120">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="e6cd3-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="e6cd3-121">-DefaultDocuments</span></span>
<span data-ttu-id="e6cd3-122">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="e6cd3-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cd3-123">-DefaultProfile</span></span>
<span data-ttu-id="e6cd3-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e6cd3-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e6cd3-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="e6cd3-126">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="e6cd3-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="e6cd3-127">-HandlerMappings</span></span>
<span data-ttu-id="e6cd3-128">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="e6cd3-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="e6cd3-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="e6cd3-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="e6cd3-130">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="e6cd3-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="e6cd3-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="e6cd3-132">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="e6cd3-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e6cd3-133">-Name</span></span>
<span data-ttu-id="e6cd3-134">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="e6cd3-134">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="e6cd3-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="e6cd3-136">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="e6cd3-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="e6cd3-137">-NumberOfWorkers</span></span>
<span data-ttu-id="e6cd3-138">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="e6cd3-138">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="e6cd3-139">-PhpVersion</span></span>
<span data-ttu-id="e6cd3-140">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="e6cd3-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="e6cd3-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="e6cd3-142">Anforderungs Ablaufverfolgung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="e6cd3-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cd3-143">-ResourceGroupName</span></span>
<span data-ttu-id="e6cd3-144">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e6cd3-144">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="e6cd3-145">-Slot</span></span>
<span data-ttu-id="e6cd3-146">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="e6cd3-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="e6cd3-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="e6cd3-148">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="e6cd3-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-149">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="e6cd3-149">-WebApp</span></span>
<span data-ttu-id="e6cd3-150">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="e6cd3-150">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="e6cd3-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="e6cd3-152">Web Sockets enabled Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="e6cd3-152">Web Sockets Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="e6cd3-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e6cd3-153">-HttpsOnly</span></span>
<span data-ttu-id="e6cd3-154">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einem vorhandenen Steckplatz</span><span class="sxs-lookup"><span data-stu-id="e6cd3-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="e6cd3-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e6cd3-155">-AssignIdentity</span></span>
<span data-ttu-id="e6cd3-156">Aktivieren/Deaktivieren von MSI für einen vorhandenen Steckplatz [Preview]</span><span class="sxs-lookup"><span data-stu-id="e6cd3-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6cd3-157">-AsJob</span></span>
<span data-ttu-id="e6cd3-158">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e6cd3-158">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cd3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cd3-159">CommonParameters</span></span>
<span data-ttu-id="e6cd3-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6cd3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cd3-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cd3-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cd3-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6cd3-162">INPUTS</span></span>

### <span data-ttu-id="e6cd3-163">Int32</span><span class="sxs-lookup"><span data-stu-id="e6cd3-163">Int32</span></span>
<span data-ttu-id="e6cd3-164">Der Parameter ' NumberOfWorkers ' akzeptiert den Wert vom Typ ' Int32 ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6cd3-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="e6cd3-165">Website</span><span class="sxs-lookup"><span data-stu-id="e6cd3-165">Site</span></span>
<span data-ttu-id="e6cd3-166">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6cd3-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e6cd3-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6cd3-167">OUTPUTS</span></span>

## <span data-ttu-id="e6cd3-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6cd3-168">NOTES</span></span>

## <span data-ttu-id="e6cd3-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6cd3-169">RELATED LINKS</span></span>

[<span data-ttu-id="e6cd3-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e6cd3-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="e6cd3-171">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e6cd3-171">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="e6cd3-172">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e6cd3-172">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="e6cd3-173">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e6cd3-173">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="e6cd3-174">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e6cd3-174">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="e6cd3-175">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e6cd3-175">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="e6cd3-176">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e6cd3-176">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
