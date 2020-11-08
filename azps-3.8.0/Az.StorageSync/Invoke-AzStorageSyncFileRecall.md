---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: fb053da61aabd9328f4ff3d848243ff9b84d6d09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003336"
---
# <span data-ttu-id="25641-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="25641-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="25641-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25641-102">SYNOPSIS</span></span>
<span data-ttu-id="25641-103">Dieser Befehl ruft alle Tiered-Dateien wieder auf den lokalen Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="25641-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="25641-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25641-104">SYNTAX</span></span>

### <span data-ttu-id="25641-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="25641-105">StringParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25641-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25641-106">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25641-107">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="25641-107">ObjectParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25641-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25641-108">DESCRIPTION</span></span>
<span data-ttu-id="25641-109">Wenn die Cloud-Tiering-Funktion auf einem Serverendpunkt (einem bestimmten Speicherort auf einem registrierten Server) aktiviert ist, kann dieser Befehl verwendet werden, um alle Tiered-Dateien an den lokalen Datenträger zurückzurufen.</span><span class="sxs-lookup"><span data-stu-id="25641-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="25641-110">Es wird dringend empfohlen, die Cloud-Tiering-Funktion auf diesem Serverendpunkt zu deaktivieren, bevor Sie mit dem Rückruf beginnen.</span><span class="sxs-lookup"><span data-stu-id="25641-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="25641-111">Wenn Tiering immer noch aktiviert ist, kann Rückruf dazu führen, dass andere Dateien abgestuft werden, was das gewünschte Ziel des gesamten Inhalts auf dem lokalen Datenträger nicht erreicht.</span><span class="sxs-lookup"><span data-stu-id="25641-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="25641-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25641-112">EXAMPLES</span></span>

### <span data-ttu-id="25641-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25641-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="25641-114">Dieser Befehl ruft rekursiv alle Tiered-Dateien ab, die sich unterhalb des Stammpfads des angegebenen Server Endpunkts befinden.</span><span class="sxs-lookup"><span data-stu-id="25641-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="25641-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="25641-115">PARAMETERS</span></span>

### <span data-ttu-id="25641-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25641-116">-AsJob</span></span>
<span data-ttu-id="25641-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="25641-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25641-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25641-118">-DefaultProfile</span></span>
<span data-ttu-id="25641-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25641-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25641-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25641-120">-InputObject</span></span>
<span data-ttu-id="25641-121">SyncGroup-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="25641-121">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="25641-122">-Name</span><span class="sxs-lookup"><span data-stu-id="25641-122">-Name</span></span>
<span data-ttu-id="25641-123">Der Name des ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="25641-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="25641-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25641-124">-PassThru</span></span>
<span data-ttu-id="25641-125">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="25641-125">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="25641-126">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="25641-126">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="25641-127">-Muster</span><span class="sxs-lookup"><span data-stu-id="25641-127">-Pattern</span></span>
<span data-ttu-id="25641-128">Muster des Datei namens</span><span class="sxs-lookup"><span data-stu-id="25641-128">Pattern of the file name</span></span>

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

### <span data-ttu-id="25641-129">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="25641-129">-RecallPath</span></span>
<span data-ttu-id="25641-130">Rückruf Pfad, der zurückgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="25641-130">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="25641-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25641-131">-ResourceGroupName</span></span>
<span data-ttu-id="25641-132">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="25641-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="25641-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="25641-133">-ResourceId</span></span>
<span data-ttu-id="25641-134">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="25641-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="25641-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="25641-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="25641-136">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="25641-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="25641-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="25641-137">-SyncGroupName</span></span>
<span data-ttu-id="25641-138">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="25641-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="25641-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25641-139">-Confirm</span></span>
<span data-ttu-id="25641-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25641-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25641-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25641-141">-WhatIf</span></span>
<span data-ttu-id="25641-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25641-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25641-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25641-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25641-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25641-144">CommonParameters</span></span>
<span data-ttu-id="25641-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25641-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25641-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25641-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25641-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25641-147">INPUTS</span></span>

### <span data-ttu-id="25641-148">System. String</span><span class="sxs-lookup"><span data-stu-id="25641-148">System.String</span></span>

### <span data-ttu-id="25641-149">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25641-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="25641-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25641-150">OUTPUTS</span></span>

### <span data-ttu-id="25641-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25641-151">System.Boolean</span></span>

## <span data-ttu-id="25641-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="25641-152">NOTES</span></span>

## <span data-ttu-id="25641-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25641-153">RELATED LINKS</span></span>
