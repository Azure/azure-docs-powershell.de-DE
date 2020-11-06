---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: 2787c1cf8a37fd5d143e95c55d3e98b625d4d82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478605"
---
# <span data-ttu-id="f7494-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="f7494-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="f7494-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7494-102">SYNOPSIS</span></span>
<span data-ttu-id="f7494-103">Gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f7494-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7494-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7494-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7494-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7494-105">DESCRIPTION</span></span>
<span data-ttu-id="f7494-106">Das Cmdlet **Grant-AzureRmDiskAccess** gewährt einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f7494-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="f7494-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7494-107">EXAMPLES</span></span>

### <span data-ttu-id="f7494-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7494-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="f7494-109">Gewähren Sie "Read"-Zugriff auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f7494-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="f7494-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7494-110">PARAMETERS</span></span>

### <span data-ttu-id="f7494-111">-Access</span><span class="sxs-lookup"><span data-stu-id="f7494-111">-Access</span></span>
<span data-ttu-id="f7494-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="f7494-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7494-113">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="f7494-113">-DiskName</span></span>
<span data-ttu-id="f7494-114">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="f7494-114">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7494-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="f7494-115">-DurationInSecond</span></span>
<span data-ttu-id="f7494-116">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f7494-116">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7494-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7494-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7494-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f7494-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7494-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7494-119">-Confirm</span></span>
<span data-ttu-id="f7494-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7494-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7494-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7494-121">-WhatIf</span></span>
<span data-ttu-id="f7494-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7494-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7494-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7494-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7494-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7494-124">CommonParameters</span></span>
<span data-ttu-id="f7494-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7494-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7494-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7494-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7494-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7494-127">INPUTS</span></span>

### <span data-ttu-id="f7494-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f7494-128">System.String</span></span>

## <span data-ttu-id="f7494-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7494-129">OUTPUTS</span></span>

### <span data-ttu-id="f7494-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7494-130">System.Object</span></span>

## <span data-ttu-id="f7494-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7494-131">NOTES</span></span>

## <span data-ttu-id="f7494-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7494-132">RELATED LINKS</span></span>

