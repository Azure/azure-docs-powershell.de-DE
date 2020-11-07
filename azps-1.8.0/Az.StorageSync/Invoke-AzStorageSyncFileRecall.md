---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/invoke-Azstoragesyncfilerecall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncFileRecall.md
ms.openlocfilehash: 5463c20274f60c2d6fb6c4807bf2c4d27da76808
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658699"
---
# <span data-ttu-id="69ac9-101">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="69ac9-101">Invoke-AzStorageSyncFileRecall</span></span>

## <span data-ttu-id="69ac9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="69ac9-103">Dieser Befehl ruft alle Tiered-Dateien wieder auf den lokalen Datenträger zurück.</span><span class="sxs-lookup"><span data-stu-id="69ac9-103">This command recalls all tiered files back to local disk.</span></span>

## <span data-ttu-id="69ac9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69ac9-104">SYNTAX</span></span>

### <span data-ttu-id="69ac9-105">Objectparameterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="69ac9-105">ObjectParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncFileRecall [-InputObject] <PSServerEndpoint> [-Pattern <String>] [-RecallPath <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ac9-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ac9-106">StringParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69ac9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69ac9-107">ResourceIdParameterSet</span></span>
```
Invoke-AzStorageSyncFileRecall [-ResourceId] <String> [-Pattern <String>] [-RecallPath <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69ac9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69ac9-108">DESCRIPTION</span></span>
<span data-ttu-id="69ac9-109">Wenn die Cloud-Tiering-Funktion auf einem Serverendpunkt (einem bestimmten Speicherort auf einem registrierten Server) aktiviert ist, kann dieser Befehl verwendet werden, um alle Tiered-Dateien an den lokalen Datenträger zurückzurufen.</span><span class="sxs-lookup"><span data-stu-id="69ac9-109">When cloud tiering is enabled on a server endpoint (a specific location on a registered server) then this command can be used to recall all tiered files to local disk.</span></span> <span data-ttu-id="69ac9-110">Es wird dringend empfohlen, die Cloud-Tiering-Funktion auf diesem Serverendpunkt zu deaktivieren, bevor Sie mit dem Rückruf beginnen.</span><span class="sxs-lookup"><span data-stu-id="69ac9-110">It is highly recommended to disable cloud tiering on this server endpoint before starting recall.</span></span> <span data-ttu-id="69ac9-111">Wenn Tiering immer noch aktiviert ist, kann Rückruf dazu führen, dass andere Dateien abgestuft werden, was das gewünschte Ziel des gesamten Inhalts auf dem lokalen Datenträger nicht erreicht.</span><span class="sxs-lookup"><span data-stu-id="69ac9-111">If tiering is still on, recall might lead to other files getting tiered which misses to achieve the desired goal of all content residing on local disk.</span></span>

## <span data-ttu-id="69ac9-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69ac9-112">EXAMPLES</span></span>

### <span data-ttu-id="69ac9-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69ac9-113">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncFileRecall -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -ServerEndpointName "myServerEndpointName"
```

<span data-ttu-id="69ac9-114">Dieser Befehl ruft rekursiv alle Tiered-Dateien ab, die sich unterhalb des Stammpfads des angegebenen Server Endpunkts befinden.</span><span class="sxs-lookup"><span data-stu-id="69ac9-114">This command recursively recalls all tiered files located under the root path of the specified server endpoint.</span></span>

## <span data-ttu-id="69ac9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="69ac9-115">PARAMETERS</span></span>

### <span data-ttu-id="69ac9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69ac9-116">-AsJob</span></span>
<span data-ttu-id="69ac9-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="69ac9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69ac9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ac9-118">-DefaultProfile</span></span>
<span data-ttu-id="69ac9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69ac9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ac9-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69ac9-120">-InputObject</span></span>
<span data-ttu-id="69ac9-121">SyncGroup-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="69ac9-121">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69ac9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="69ac9-122">-Name</span></span>
<span data-ttu-id="69ac9-123">Der Name des ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="69ac9-123">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="69ac9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69ac9-124">-PassThru</span></span>
<span data-ttu-id="69ac9-125">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="69ac9-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="69ac9-126">-Muster</span><span class="sxs-lookup"><span data-stu-id="69ac9-126">-Pattern</span></span>
<span data-ttu-id="69ac9-127">Muster des Datei namens</span><span class="sxs-lookup"><span data-stu-id="69ac9-127">Pattern of the file name</span></span>

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

### <span data-ttu-id="69ac9-128">-RecallPath</span><span class="sxs-lookup"><span data-stu-id="69ac9-128">-RecallPath</span></span>
<span data-ttu-id="69ac9-129">Rückruf Pfad, der zurückgerufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="69ac9-129">Recall path which need to be recalled.</span></span>

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

### <span data-ttu-id="69ac9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ac9-130">-ResourceGroupName</span></span>
<span data-ttu-id="69ac9-131">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69ac9-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="69ac9-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="69ac9-132">-ResourceId</span></span>
<span data-ttu-id="69ac9-133">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="69ac9-133">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="69ac9-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="69ac9-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="69ac9-135">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="69ac9-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="69ac9-136">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="69ac9-136">-SyncGroupName</span></span>
<span data-ttu-id="69ac9-137">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="69ac9-137">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="69ac9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ac9-138">CommonParameters</span></span>
<span data-ttu-id="69ac9-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ac9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ac9-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ac9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ac9-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69ac9-141">INPUTS</span></span>

### <span data-ttu-id="69ac9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="69ac9-142">System.String</span></span>

### <span data-ttu-id="69ac9-143">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="69ac9-143">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="69ac9-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69ac9-144">OUTPUTS</span></span>

### <span data-ttu-id="69ac9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69ac9-145">System.Boolean</span></span>

## <span data-ttu-id="69ac9-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="69ac9-146">NOTES</span></span>

## <span data-ttu-id="69ac9-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69ac9-147">RELATED LINKS</span></span>
