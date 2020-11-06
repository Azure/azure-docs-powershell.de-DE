---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502302"
---
# <span data-ttu-id="9a727-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a727-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="9a727-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a727-102">SYNOPSIS</span></span>
<span data-ttu-id="9a727-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9a727-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a727-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a727-104">SYNTAX</span></span>

### <span data-ttu-id="9a727-105">S1</span><span class="sxs-lookup"><span data-stu-id="9a727-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a727-106">S2</span><span class="sxs-lookup"><span data-stu-id="9a727-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a727-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a727-107">DESCRIPTION</span></span>
<span data-ttu-id="9a727-108">Das Cmdlet " **Set-AzureRmWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="9a727-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="9a727-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a727-109">EXAMPLES</span></span>

### <span data-ttu-id="9a727-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a727-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="9a727-111">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="9a727-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="9a727-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a727-112">PARAMETERS</span></span>

### <span data-ttu-id="9a727-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9a727-113">-AppServicePlan</span></span>
<span data-ttu-id="9a727-114">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="9a727-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="9a727-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="9a727-115">-AppSettings</span></span>
<span data-ttu-id="9a727-116">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9a727-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="9a727-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="9a727-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="9a727-118">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="9a727-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="9a727-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="9a727-119">-ConnectionStrings</span></span>
<span data-ttu-id="9a727-120">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="9a727-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="9a727-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="9a727-121">-DefaultDocuments</span></span>
<span data-ttu-id="9a727-122">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="9a727-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="9a727-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a727-123">-DefaultProfile</span></span>
<span data-ttu-id="9a727-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a727-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a727-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9a727-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="9a727-126">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="9a727-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="9a727-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="9a727-127">-HandlerMappings</span></span>
<span data-ttu-id="9a727-128">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="9a727-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="9a727-129">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="9a727-129">-HostNames</span></span>
<span data-ttu-id="9a727-130">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="9a727-130">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="9a727-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9a727-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="9a727-132">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="9a727-132">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="9a727-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="9a727-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="9a727-134">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="9a727-134">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="9a727-135">-Name</span><span class="sxs-lookup"><span data-stu-id="9a727-135">-Name</span></span>
<span data-ttu-id="9a727-136">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="9a727-136">WebApp Name</span></span>

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

### <span data-ttu-id="9a727-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="9a727-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="9a727-138">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="9a727-138">Net Framework Version</span></span>

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

### <span data-ttu-id="9a727-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="9a727-139">-NumberOfWorkers</span></span>
<span data-ttu-id="9a727-140">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="9a727-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="9a727-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="9a727-141">-PhpVersion</span></span>
<span data-ttu-id="9a727-142">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="9a727-142">Php Version</span></span>

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

### <span data-ttu-id="9a727-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="9a727-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="9a727-144">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="9a727-144">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="9a727-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a727-145">-ResourceGroupName</span></span>
<span data-ttu-id="9a727-146">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9a727-146">Resource Group Name</span></span>

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

### <span data-ttu-id="9a727-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="9a727-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="9a727-148">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="9a727-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="9a727-149">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="9a727-149">-WebApp</span></span>
<span data-ttu-id="9a727-150">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="9a727-150">WebApp Object</span></span>

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

### <span data-ttu-id="9a727-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="9a727-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="9a727-152">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="9a727-152">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="9a727-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a727-153">-AsJob</span></span>
<span data-ttu-id="9a727-154">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9a727-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a727-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a727-155">CommonParameters</span></span>
<span data-ttu-id="9a727-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a727-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a727-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a727-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a727-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a727-158">INPUTS</span></span>

### <span data-ttu-id="9a727-159">Int32</span><span class="sxs-lookup"><span data-stu-id="9a727-159">Int32</span></span>
<span data-ttu-id="9a727-160">Der Parameter ' NumberOfWorkers ' akzeptiert den Wert vom Typ ' Int32 ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a727-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="9a727-161">Website</span><span class="sxs-lookup"><span data-stu-id="9a727-161">Site</span></span>
<span data-ttu-id="9a727-162">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="9a727-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9a727-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a727-163">OUTPUTS</span></span>

## <span data-ttu-id="9a727-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a727-164">NOTES</span></span>

## <span data-ttu-id="9a727-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a727-165">RELATED LINKS</span></span>

[<span data-ttu-id="9a727-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a727-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="9a727-167">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a727-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="9a727-168">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a727-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="9a727-169">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a727-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="9a727-170">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a727-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="9a727-171">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9a727-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
