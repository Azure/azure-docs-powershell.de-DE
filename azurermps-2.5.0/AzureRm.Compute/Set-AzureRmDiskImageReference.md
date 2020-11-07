---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
ms.openlocfilehash: cd0a66d8f8d777df9a8ebc3791643234f0d15fb0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849715"
---
# <span data-ttu-id="b5378-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="b5378-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="b5378-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5378-102">SYNOPSIS</span></span>
<span data-ttu-id="b5378-103">Legt die Bildverweis Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="b5378-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5378-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5378-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5378-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5378-105">DESCRIPTION</span></span>
<span data-ttu-id="b5378-106">Das Cmdlet " **Set-AzureRmDiskImageReference** " legt die Bildverweis Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="b5378-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="b5378-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5378-107">EXAMPLES</span></span>

### <span data-ttu-id="b5378-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b5378-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="b5378-109">Der erste Befehl erstellt ein lokales Datenträgerobjekt mit einer Größe von 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="b5378-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b5378-110">Außerdem wird der Windows-Betriebssystemtyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b5378-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="b5378-111">Der zweite Befehl legt die Bild-ID und die logische Einheitsnummer 0 für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="b5378-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="b5378-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b5378-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b5378-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5378-113">PARAMETERS</span></span>

### <span data-ttu-id="b5378-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5378-114">-DefaultProfile</span></span>
<span data-ttu-id="b5378-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5378-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5378-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="b5378-116">-Disk</span></span>
<span data-ttu-id="b5378-117">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b5378-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5378-118">-ID</span><span class="sxs-lookup"><span data-stu-id="b5378-118">-Id</span></span>
<span data-ttu-id="b5378-119">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="b5378-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="b5378-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="b5378-120">-Lun</span></span>
<span data-ttu-id="b5378-121">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="b5378-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="b5378-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5378-122">-Confirm</span></span>
<span data-ttu-id="b5378-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5378-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5378-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5378-124">-WhatIf</span></span>
<span data-ttu-id="b5378-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5378-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5378-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5378-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5378-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5378-127">CommonParameters</span></span>
<span data-ttu-id="b5378-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5378-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5378-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5378-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5378-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5378-130">INPUTS</span></span>

### <span data-ttu-id="b5378-131">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="b5378-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="b5378-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b5378-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b5378-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5378-133">OUTPUTS</span></span>

### <span data-ttu-id="b5378-134">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="b5378-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="b5378-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5378-135">NOTES</span></span>

## <span data-ttu-id="b5378-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5378-136">RELATED LINKS</span></span>

