---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366692"
---
# <span data-ttu-id="171f1-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="171f1-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="171f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="171f1-102">SYNOPSIS</span></span>
<span data-ttu-id="171f1-103">Dieser Befehl ruft alle mehrstufigen Dateien auf den lokalen Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="171f1-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="171f1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="171f1-104">SYNTAX</span></span>

### <span data-ttu-id="171f1-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="171f1-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="171f1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="171f1-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="171f1-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="171f1-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="171f1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="171f1-108">DESCRIPTION</span></span>
<span data-ttu-id="171f1-109">Wenn die Cloud tiering auf einem Serverendpunkt (einem bestimmten Speicherort auf einem registrierten Server) aktiviert ist, kann dieser Befehl verwendet werden, um alle mehrstufigen Dateien auf den lokalen Datenträger zurückrufen.</span><span class="sxs-lookup"><span data-stu-id="171f1-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="171f1-110">Es wird dringend empfohlen, die Cloud tiering auf diesem Serverendpunkt zu deaktivieren, bevor Sie den Rückruf starten.</span><span class="sxs-lookup"><span data-stu-id="171f1-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="171f1-111">Wenn die Gestuftierung weiterhin besteht, kann der Rückruf dazu führen, dass andere Dateien mehrstufiger Werden, wodurch das gewünschte Ziel aller Inhalte, die sich auf dem lokalen Datenträger aufhalten, nicht erreicht werden können.</span><span class="sxs-lookup"><span data-stu-id="171f1-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="171f1-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="171f1-112">EXAMPLES</span></span>

### <span data-ttu-id="171f1-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="171f1-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="171f1-114">Dieser Befehl ruft rekursiv alle mehrstufigen Dateien zurück, die sich unter dem Stammpfad des angegebenen Serverendpunkts befinden.</span><span class="sxs-lookup"><span data-stu-id="171f1-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="171f1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="171f1-115">PARAMETERS</span></span>

### <span data-ttu-id="171f1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="171f1-116">-AsJob</span></span>
<span data-ttu-id="171f1-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="171f1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="171f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="171f1-118">-DefaultProfile</span></span>
<span data-ttu-id="171f1-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="171f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="171f1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="171f1-120">-InputObject</span></span>
<span data-ttu-id="171f1-121">SyncGroup-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="171f1-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer, ServerEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="171f1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="171f1-122">-Name</span></span>
<span data-ttu-id="171f1-123">Der Name von ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="171f1-123">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171f1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="171f1-124">-PassThru</span></span>
<span data-ttu-id="171f1-125">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="171f1-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="171f1-126">Wenn Sie den Parameter "PassThru" angeben, schreibt das Cmdlet nach erfolgreicher Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="171f1-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="171f1-127">-Pattern</span><span class="sxs-lookup"><span data-stu-id="171f1-127">-Pattern</span></span>
<span data-ttu-id="171f1-128">Muster des Dateinamens</span><span class="sxs-lookup"><span data-stu-id="171f1-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="171f1-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="171f1-129">-RecallPath</span></span>
<span data-ttu-id="171f1-130">Zurückrufpfad, der zurückgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="171f1-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="171f1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="171f1-131">-ResourceGroupName</span></span>
<span data-ttu-id="171f1-132">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="171f1-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171f1-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="171f1-133">-ResourceId</span></span>
<span data-ttu-id="171f1-134">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="171f1-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="171f1-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="171f1-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="171f1-136">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="171f1-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171f1-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="171f1-137">-SyncGroupName</span></span>
<span data-ttu-id="171f1-138">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="171f1-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171f1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="171f1-139">-Confirm</span></span>
<span data-ttu-id="171f1-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="171f1-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171f1-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="171f1-141">-WhatIf</span></span>
<span data-ttu-id="171f1-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="171f1-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="171f1-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="171f1-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="171f1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171f1-144">CommonParameters</span></span>
<span data-ttu-id="171f1-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="171f1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171f1-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="171f1-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171f1-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="171f1-147">INPUTS</span></span>

### <span data-ttu-id="171f1-148">System.String</span><span class="sxs-lookup"><span data-stu-id="171f1-148">System.String</span></span>

### <span data-ttu-id="171f1-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="171f1-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="171f1-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="171f1-150">OUTPUTS</span></span>

### <span data-ttu-id="171f1-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="171f1-151">System.Boolean</span></span>

## <span data-ttu-id="171f1-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="171f1-152">NOTES</span></span>

## <span data-ttu-id="171f1-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="171f1-153">RELATED LINKS</span></span>
