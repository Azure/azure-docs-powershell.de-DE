---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 78a6c3bf85fae4fab9c5b9a06c366760b55804fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009996"
---
# <span data-ttu-id="35616-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="35616-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="35616-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35616-102">SYNOPSIS</span></span>
<span data-ttu-id="35616-103">Legt die Bildverweis Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="35616-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="35616-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35616-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35616-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35616-105">DESCRIPTION</span></span>
<span data-ttu-id="35616-106">Das Cmdlet " **Set-AzDiskImageReference** " legt die Bildverweis Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="35616-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="35616-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35616-107">EXAMPLES</span></span>

### <span data-ttu-id="35616-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35616-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="35616-109">Der erste Befehl erstellt ein lokales Datenträgerobjekt mit einer Größe von 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="35616-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="35616-110">Außerdem wird der Windows-Betriebssystemtyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="35616-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="35616-111">Der zweite Befehl legt die Bild-ID und die logische Einheitsnummer 0 für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="35616-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="35616-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="35616-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="35616-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="35616-113">PARAMETERS</span></span>

### <span data-ttu-id="35616-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35616-114">-DefaultProfile</span></span>
<span data-ttu-id="35616-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35616-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35616-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="35616-116">-Disk</span></span>
<span data-ttu-id="35616-117">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="35616-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35616-118">-ID</span><span class="sxs-lookup"><span data-stu-id="35616-118">-Id</span></span>
<span data-ttu-id="35616-119">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="35616-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="35616-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="35616-120">-Lun</span></span>
<span data-ttu-id="35616-121">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="35616-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="35616-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35616-122">-Confirm</span></span>
<span data-ttu-id="35616-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35616-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35616-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35616-124">-WhatIf</span></span>
<span data-ttu-id="35616-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35616-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35616-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35616-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35616-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35616-127">CommonParameters</span></span>
<span data-ttu-id="35616-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35616-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35616-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35616-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35616-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35616-130">INPUTS</span></span>

### <span data-ttu-id="35616-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="35616-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="35616-132">System. String</span><span class="sxs-lookup"><span data-stu-id="35616-132">System.String</span></span>

### <span data-ttu-id="35616-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="35616-133">System.Int32</span></span>

## <span data-ttu-id="35616-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35616-134">OUTPUTS</span></span>

### <span data-ttu-id="35616-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="35616-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="35616-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="35616-136">NOTES</span></span>

## <span data-ttu-id="35616-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35616-137">RELATED LINKS</span></span>
