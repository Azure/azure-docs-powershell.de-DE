---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: fa6b3e16fd137453229232405d31cd7665ccd18e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478581"
---
# <span data-ttu-id="6d875-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="6d875-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="6d875-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d875-102">SYNOPSIS</span></span>
<span data-ttu-id="6d875-103">Legt die Bildverweis Eigenschaften für ein Aktualisierungs Objekt für Snapshots fest.</span><span class="sxs-lookup"><span data-stu-id="6d875-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d875-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d875-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <SnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d875-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d875-105">DESCRIPTION</span></span>
<span data-ttu-id="6d875-106">Das Cmdlet " **Set-AzureRmSnapshotUpdateImageReference** " legt die Bildverweis Eigenschaften für ein Aktualisierungs Objekt für Snapshots fest.</span><span class="sxs-lookup"><span data-stu-id="6d875-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="6d875-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d875-107">EXAMPLES</span></span>

### <span data-ttu-id="6d875-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d875-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="6d875-109">Mit dem ersten Befehl wird ein lokales Snapshot-Update Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="6d875-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="6d875-110">Außerdem wird der Windows-Betriebssystemtyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d875-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="6d875-111">Der zweite Befehl legt die Bild-ID und die logische Einheitsnummer 0 für das Snapshot-Update-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="6d875-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="6d875-112">Der letzte Befehl übernimmt das Aktualisierungs Objekt für Snapshots und aktualisiert einen vorhandenen Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6d875-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6d875-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d875-113">PARAMETERS</span></span>

### <span data-ttu-id="6d875-114">-ID</span><span class="sxs-lookup"><span data-stu-id="6d875-114">-Id</span></span>
<span data-ttu-id="6d875-115">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="6d875-115">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d875-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="6d875-116">-Lun</span></span>
<span data-ttu-id="6d875-117">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="6d875-117">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d875-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6d875-118">-SnapshotUpdate</span></span>
<span data-ttu-id="6d875-119">Gibt ein lokales Aktualisierungs Objekt für Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="6d875-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d875-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d875-120">-Confirm</span></span>
<span data-ttu-id="6d875-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d875-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d875-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d875-122">-WhatIf</span></span>
<span data-ttu-id="6d875-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d875-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d875-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d875-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d875-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d875-125">CommonParameters</span></span>
<span data-ttu-id="6d875-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d875-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d875-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d875-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d875-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d875-128">INPUTS</span></span>

### <span data-ttu-id="6d875-129">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6d875-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="6d875-130">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6d875-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6d875-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d875-131">OUTPUTS</span></span>

### <span data-ttu-id="6d875-132">Microsoft. Azure. Management. Compute. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6d875-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="6d875-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d875-133">NOTES</span></span>

## <span data-ttu-id="6d875-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d875-134">RELATED LINKS</span></span>

