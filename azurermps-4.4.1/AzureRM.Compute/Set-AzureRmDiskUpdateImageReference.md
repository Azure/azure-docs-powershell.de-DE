---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 777216f6969e661721785601a21ee9604d5eec94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665101"
---
# <span data-ttu-id="bdddc-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="bdddc-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="bdddc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bdddc-102">SYNOPSIS</span></span>
<span data-ttu-id="bdddc-103">Legt die Bildverweis Eigenschaften für ein Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="bdddc-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdddc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdddc-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <PSDiskUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdddc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bdddc-105">DESCRIPTION</span></span>
<span data-ttu-id="bdddc-106">Das Cmdlet " **Set-AzureRmDiskUpdateImageReference** " legt die Bildverweis Eigenschaften für ein Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="bdddc-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="bdddc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bdddc-107">EXAMPLES</span></span>

### <span data-ttu-id="bdddc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bdddc-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="bdddc-109">Der erste Befehl erstellt ein lokales Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="bdddc-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="bdddc-110">Außerdem wird der Windows-Betriebssystemtyp festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bdddc-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="bdddc-111">Der zweite Befehl legt die Bild-ID und die logische Einheitsnummer 0 für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="bdddc-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="bdddc-112">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="bdddc-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bdddc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdddc-113">PARAMETERS</span></span>

### <span data-ttu-id="bdddc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdddc-114">-DefaultProfile</span></span>
<span data-ttu-id="bdddc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bdddc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdddc-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bdddc-116">-DiskUpdate</span></span>
<span data-ttu-id="bdddc-117">Gibt ein lokales Datenträger Aktualisierungs Objekt an.</span><span class="sxs-lookup"><span data-stu-id="bdddc-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdddc-118">-ID</span><span class="sxs-lookup"><span data-stu-id="bdddc-118">-Id</span></span>
<span data-ttu-id="bdddc-119">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="bdddc-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="bdddc-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="bdddc-120">-Lun</span></span>
<span data-ttu-id="bdddc-121">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="bdddc-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdddc-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bdddc-122">-Confirm</span></span>
<span data-ttu-id="bdddc-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bdddc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdddc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdddc-124">-WhatIf</span></span>
<span data-ttu-id="bdddc-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdddc-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdddc-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bdddc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdddc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdddc-127">CommonParameters</span></span>
<span data-ttu-id="bdddc-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdddc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdddc-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdddc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdddc-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bdddc-130">INPUTS</span></span>

### <span data-ttu-id="bdddc-131">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bdddc-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="bdddc-132">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bdddc-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bdddc-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bdddc-133">OUTPUTS</span></span>

### <span data-ttu-id="bdddc-134">Microsoft. Azure. Management. Compute. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="bdddc-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="bdddc-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="bdddc-135">NOTES</span></span>

## <span data-ttu-id="bdddc-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bdddc-136">RELATED LINKS</span></span>

