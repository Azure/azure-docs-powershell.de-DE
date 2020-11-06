---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479825"
---
# <span data-ttu-id="0f8a9-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f8a9-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="0f8a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0f8a9-103">Ändert eine Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="0f8a9-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f8a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f8a9-104">SYNTAX</span></span>

### <span data-ttu-id="0f8a9-105">S1</span><span class="sxs-lookup"><span data-stu-id="0f8a9-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f8a9-106">S2</span><span class="sxs-lookup"><span data-stu-id="0f8a9-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f8a9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f8a9-107">DESCRIPTION</span></span>
<span data-ttu-id="0f8a9-108">Das Cmdlet " **Set-AzureRmWebApp** " legt eine Azure Web App fest.</span><span class="sxs-lookup"><span data-stu-id="0f8a9-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="0f8a9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f8a9-109">EXAMPLES</span></span>

### <span data-ttu-id="0f8a9-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f8a9-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="0f8a9-111">Mit diesem Befehl wird HttpLoggingEnabled für Web-App-ContosoWebApp festgelegt, die mit der Ressourcengruppe Standard verknüpft sind – Web-westus</span><span class="sxs-lookup"><span data-stu-id="0f8a9-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="0f8a9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f8a9-112">PARAMETERS</span></span>

### <span data-ttu-id="0f8a9-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0f8a9-113">-AppServicePlan</span></span>
<span data-ttu-id="0f8a9-114">Name des App-Service Plans</span><span class="sxs-lookup"><span data-stu-id="0f8a9-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="0f8a9-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="0f8a9-115">-AppSettings</span></span>
<span data-ttu-id="0f8a9-116">Hashtable für App-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0f8a9-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="0f8a9-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="0f8a9-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="0f8a9-118">Name des Ziel Steckplatzes für den automatischen Austausch</span><span class="sxs-lookup"><span data-stu-id="0f8a9-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="0f8a9-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="0f8a9-119">-ConnectionStrings</span></span>
<span data-ttu-id="0f8a9-120">Hashtable für Verbindungszeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="0f8a9-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="0f8a9-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="0f8a9-121">-DefaultDocuments</span></span>
<span data-ttu-id="0f8a9-122">Standard-Zeichenfolgen Array für Dokumente</span><span class="sxs-lookup"><span data-stu-id="0f8a9-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="0f8a9-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0f8a9-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="0f8a9-124">Detaillierte Fehlerprotokollierung aktiviert boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0f8a9-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="0f8a9-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="0f8a9-125">-HandlerMappings</span></span>
<span data-ttu-id="0f8a9-126">Handler-Zuordnungen, IList</span><span class="sxs-lookup"><span data-stu-id="0f8a9-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="0f8a9-127">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="0f8a9-127">-HostNames</span></span>
<span data-ttu-id="0f8a9-128">Host-hostnames-Zeichenfolge Array</span><span class="sxs-lookup"><span data-stu-id="0f8a9-128">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="0f8a9-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="0f8a9-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="0f8a9-130">HttpLoggingEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0f8a9-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="0f8a9-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="0f8a9-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="0f8a9-132">Name des verwalteten Pipeline Modus</span><span class="sxs-lookup"><span data-stu-id="0f8a9-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="0f8a9-133">-Name</span><span class="sxs-lookup"><span data-stu-id="0f8a9-133">-Name</span></span>
<span data-ttu-id="0f8a9-134">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0f8a9-134">WebApp Name</span></span>

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

### <span data-ttu-id="0f8a9-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="0f8a9-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="0f8a9-136">NET Framework-Version</span><span class="sxs-lookup"><span data-stu-id="0f8a9-136">Net Framework Version</span></span>

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

### <span data-ttu-id="0f8a9-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="0f8a9-137">-NumberOfWorkers</span></span>
<span data-ttu-id="0f8a9-138">Die Anzahl der Arbeitskräfte, die zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="0f8a9-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="0f8a9-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="0f8a9-139">-PhpVersion</span></span>
<span data-ttu-id="0f8a9-140">PHP-Version</span><span class="sxs-lookup"><span data-stu-id="0f8a9-140">Php Version</span></span>

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

### <span data-ttu-id="0f8a9-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="0f8a9-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="0f8a9-142">Anforderungs Ablaufverfolgung aktiviert</span><span class="sxs-lookup"><span data-stu-id="0f8a9-142">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="0f8a9-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f8a9-143">-ResourceGroupName</span></span>
<span data-ttu-id="0f8a9-144">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0f8a9-144">Resource Group Name</span></span>

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

### <span data-ttu-id="0f8a9-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="0f8a9-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="0f8a9-146">Verwenden des 32-Bit-Workerprozess-booleschen Werts</span><span class="sxs-lookup"><span data-stu-id="0f8a9-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="0f8a9-147">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="0f8a9-147">-WebApp</span></span>
<span data-ttu-id="0f8a9-148">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="0f8a9-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f8a9-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="0f8a9-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="0f8a9-150">WebSocketsEnabled-boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="0f8a9-150">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="0f8a9-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8a9-151">-DefaultProfile</span></span>
<span data-ttu-id="0f8a9-152">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f8a9-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f8a9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8a9-153">CommonParameters</span></span>
<span data-ttu-id="0f8a9-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f8a9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8a9-155">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8a9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8a9-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f8a9-156">INPUTS</span></span>

### <span data-ttu-id="0f8a9-157">Int32</span><span class="sxs-lookup"><span data-stu-id="0f8a9-157">Int32</span></span>
<span data-ttu-id="0f8a9-158">Der Parameter ' NumberOfWorkers ' akzeptiert den Wert vom Typ ' Int32 ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f8a9-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="0f8a9-159">Website</span><span class="sxs-lookup"><span data-stu-id="0f8a9-159">Site</span></span>
<span data-ttu-id="0f8a9-160">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f8a9-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0f8a9-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f8a9-161">OUTPUTS</span></span>

## <span data-ttu-id="0f8a9-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f8a9-162">NOTES</span></span>

## <span data-ttu-id="0f8a9-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f8a9-163">RELATED LINKS</span></span>

[<span data-ttu-id="0f8a9-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f8a9-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="0f8a9-165">Neu – AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f8a9-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="0f8a9-166">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f8a9-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0f8a9-167">Neustart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f8a9-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0f8a9-168">Anfang-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f8a9-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="0f8a9-169">Stopp-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f8a9-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
