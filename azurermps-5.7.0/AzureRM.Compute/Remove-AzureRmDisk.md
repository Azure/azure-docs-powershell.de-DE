---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 10150d7941aa3b17a0a7d4447ff0a57e3d04a516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478586"
---
# <span data-ttu-id="3ceb4-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="3ceb4-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="3ceb4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ceb4-102">SYNOPSIS</span></span>
<span data-ttu-id="3ceb4-103">Entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ceb4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ceb4-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ceb4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ceb4-105">DESCRIPTION</span></span>
<span data-ttu-id="3ceb4-106">Das Cmdlet **Remove-AzureRmDisk** entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="3ceb4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ceb4-107">EXAMPLES</span></span>

### <span data-ttu-id="3ceb4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3ceb4-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="3ceb4-109">Dieser Befehl entfernt den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3ceb4-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3ceb4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ceb4-110">PARAMETERS</span></span>

### <span data-ttu-id="3ceb4-111">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="3ceb4-111">-DiskName</span></span>
<span data-ttu-id="3ceb4-112">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="3ceb4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3ceb4-113">-Force</span></span>
<span data-ttu-id="3ceb4-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ceb4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ceb4-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ceb4-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3ceb4-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ceb4-117">-Confirm</span></span>
<span data-ttu-id="3ceb4-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ceb4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ceb4-119">-WhatIf</span></span>
<span data-ttu-id="3ceb4-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ceb4-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ceb4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ceb4-122">CommonParameters</span></span>
<span data-ttu-id="3ceb4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ceb4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ceb4-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ceb4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ceb4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ceb4-125">INPUTS</span></span>

### <span data-ttu-id="3ceb4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3ceb4-126">System.String</span></span>

## <span data-ttu-id="3ceb4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ceb4-127">OUTPUTS</span></span>

### <span data-ttu-id="3ceb4-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="3ceb4-128">System.Object</span></span>

## <span data-ttu-id="3ceb4-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ceb4-129">NOTES</span></span>

## <span data-ttu-id="3ceb4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ceb4-130">RELATED LINKS</span></span>

