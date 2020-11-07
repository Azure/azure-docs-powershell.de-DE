---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: d722c378e246fa175741c91092d99415275f094e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848959"
---
# <span data-ttu-id="91381-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91381-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="91381-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="91381-102">SYNOPSIS</span></span>
<span data-ttu-id="91381-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="91381-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91381-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="91381-104">SYNTAX</span></span>

### <span data-ttu-id="91381-105">S1</span><span class="sxs-lookup"><span data-stu-id="91381-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91381-106">S2</span><span class="sxs-lookup"><span data-stu-id="91381-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91381-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91381-107">DESCRIPTION</span></span>
<span data-ttu-id="91381-108">Das Cmdlet " **Set-AzureRmWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="91381-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="91381-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="91381-109">EXAMPLES</span></span>

### <span data-ttu-id="91381-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="91381-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="91381-111">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="91381-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="91381-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="91381-112">PARAMETERS</span></span>

### <span data-ttu-id="91381-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="91381-113">-AppServicePlan</span></span>
<span data-ttu-id="91381-114">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="91381-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="91381-115">-AppSettings</span></span>
<span data-ttu-id="91381-116">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="91381-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91381-117">-AsJob</span></span>
<span data-ttu-id="91381-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="91381-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91381-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="91381-119">-AssignIdentity</span></span>
<span data-ttu-id="91381-120">Aktivieren/Deaktivieren von MSI für eine vorhandene Azure-webfunctionapp [Preview]</span><span class="sxs-lookup"><span data-stu-id="91381-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

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

### <span data-ttu-id="91381-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="91381-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="91381-122">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="91381-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="91381-123">-ConnectionStrings</span></span>
<span data-ttu-id="91381-124">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="91381-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="91381-125">-DefaultDocuments</span></span>
<span data-ttu-id="91381-126">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="91381-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91381-127">-DefaultProfile</span></span>
<span data-ttu-id="91381-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="91381-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91381-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="91381-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="91381-130">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="91381-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="91381-131">-HandlerMappings</span></span>
<span data-ttu-id="91381-132">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="91381-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="91381-133">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="91381-133">-HostNames</span></span>
<span data-ttu-id="91381-134">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="91381-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="91381-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="91381-136">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="91381-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="91381-137">-HttpsOnly</span></span>
<span data-ttu-id="91381-138">Aktivieren/Deaktivieren der Umleitung des gesamten Datenverkehrs an HTTPS auf einer vorhandenen Azure-webfunctionapp</span><span class="sxs-lookup"><span data-stu-id="91381-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="91381-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="91381-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="91381-140">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="91381-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-141">-Name</span><span class="sxs-lookup"><span data-stu-id="91381-141">-Name</span></span>
<span data-ttu-id="91381-142">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="91381-142">WebApp Name</span></span>

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

### <span data-ttu-id="91381-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="91381-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="91381-144">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="91381-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="91381-145">-NumberOfWorkers</span></span>
<span data-ttu-id="91381-146">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="91381-146">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="91381-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="91381-147">-PhpVersion</span></span>
<span data-ttu-id="91381-148">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="91381-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="91381-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="91381-150">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="91381-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91381-151">-ResourceGroupName</span></span>
<span data-ttu-id="91381-152">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="91381-152">Resource Group Name</span></span>

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

### <span data-ttu-id="91381-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="91381-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="91381-154">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="91381-154">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="91381-155">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="91381-155">-WebApp</span></span>
<span data-ttu-id="91381-156">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="91381-156">WebApp Object</span></span>

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

### <span data-ttu-id="91381-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="91381-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="91381-158">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="91381-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91381-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91381-159">CommonParameters</span></span>
<span data-ttu-id="91381-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91381-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91381-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91381-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91381-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="91381-162">INPUTS</span></span>

### <span data-ttu-id="91381-163">Int32</span><span class="sxs-lookup"><span data-stu-id="91381-163">Int32</span></span>
<span data-ttu-id="91381-164">Der Parameter ' NumberOfWorkers ' akzeptiert den Wert vom Typ ' Int32 ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="91381-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="91381-165">Website</span><span class="sxs-lookup"><span data-stu-id="91381-165">Site</span></span>
<span data-ttu-id="91381-166">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="91381-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="91381-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="91381-167">OUTPUTS</span></span>

## <span data-ttu-id="91381-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="91381-168">NOTES</span></span>

## <span data-ttu-id="91381-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="91381-169">RELATED LINKS</span></span>

[<span data-ttu-id="91381-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91381-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="91381-171">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91381-171">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="91381-172">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91381-172">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="91381-173">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91381-173">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="91381-174">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91381-174">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="91381-175">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="91381-175">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
