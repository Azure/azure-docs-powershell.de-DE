---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005096"
---
# <span data-ttu-id="66769-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="66769-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="66769-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66769-102">SYNOPSIS</span></span>
<span data-ttu-id="66769-103">Legt die Bildverweis Eigenschaften für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="66769-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="66769-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66769-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66769-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66769-105">DESCRIPTION</span></span>
<span data-ttu-id="66769-106">Das Cmdlet " **Set-AzSnapshotImageReference** " legt die Bildverweis Eigenschaften für ein Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="66769-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="66769-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66769-107">EXAMPLES</span></span>

### <span data-ttu-id="66769-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66769-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="66769-109">Der erste Befehl erstellt ein lokales snapshotobjekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="66769-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="66769-110">Außerdem wird der Windows-Betriebssystemtyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="66769-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="66769-111">Der zweite Befehl legt die Bild-ID und die logische Einheitsnummer 0 für das Snapshot-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="66769-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="66769-112">Der letzte Befehl übernimmt das Snapshot-Objekt und erstellt einen Schnappschuss mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="66769-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="66769-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="66769-113">PARAMETERS</span></span>

### <span data-ttu-id="66769-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66769-114">-DefaultProfile</span></span>
<span data-ttu-id="66769-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66769-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66769-116">-ID</span><span class="sxs-lookup"><span data-stu-id="66769-116">-Id</span></span>
<span data-ttu-id="66769-117">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="66769-117">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66769-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="66769-118">-Lun</span></span>
<span data-ttu-id="66769-119">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="66769-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66769-120">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="66769-120">-Snapshot</span></span>
<span data-ttu-id="66769-121">Gibt ein lokales Snapshot-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="66769-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66769-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66769-122">-Confirm</span></span>
<span data-ttu-id="66769-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66769-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66769-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66769-124">-WhatIf</span></span>
<span data-ttu-id="66769-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66769-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66769-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66769-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66769-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66769-127">CommonParameters</span></span>
<span data-ttu-id="66769-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66769-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66769-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66769-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66769-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66769-130">INPUTS</span></span>

### <span data-ttu-id="66769-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="66769-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="66769-132">System. String</span><span class="sxs-lookup"><span data-stu-id="66769-132">System.String</span></span>

### <span data-ttu-id="66769-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="66769-133">System.Int32</span></span>

## <span data-ttu-id="66769-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66769-134">OUTPUTS</span></span>

### <span data-ttu-id="66769-135">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="66769-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="66769-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="66769-136">NOTES</span></span>

## <span data-ttu-id="66769-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66769-137">RELATED LINKS</span></span>
