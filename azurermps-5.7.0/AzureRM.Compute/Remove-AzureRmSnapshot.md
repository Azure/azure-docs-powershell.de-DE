---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483094"
---
# <span data-ttu-id="962ae-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="962ae-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="962ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="962ae-102">SYNOPSIS</span></span>
<span data-ttu-id="962ae-103">Entfernt einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="962ae-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="962ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="962ae-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="962ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="962ae-105">DESCRIPTION</span></span>
<span data-ttu-id="962ae-106">Das Cmdlet **Remove-AzureRmSnapshot** entfernt einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="962ae-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="962ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="962ae-107">EXAMPLES</span></span>

### <span data-ttu-id="962ae-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="962ae-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="962ae-109">Dieser Befehl entfernt den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="962ae-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="962ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="962ae-110">PARAMETERS</span></span>

### <span data-ttu-id="962ae-111">-Force</span><span class="sxs-lookup"><span data-stu-id="962ae-111">-Force</span></span>
<span data-ttu-id="962ae-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="962ae-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="962ae-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="962ae-113">-ResourceGroupName</span></span>
<span data-ttu-id="962ae-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="962ae-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="962ae-115">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="962ae-115">-SnapshotName</span></span>
<span data-ttu-id="962ae-116">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="962ae-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="962ae-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="962ae-117">-Confirm</span></span>
<span data-ttu-id="962ae-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="962ae-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="962ae-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962ae-119">-WhatIf</span></span>
<span data-ttu-id="962ae-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="962ae-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="962ae-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="962ae-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="962ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962ae-122">CommonParameters</span></span>
<span data-ttu-id="962ae-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="962ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962ae-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962ae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962ae-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="962ae-125">INPUTS</span></span>

### <span data-ttu-id="962ae-126">System. String</span><span class="sxs-lookup"><span data-stu-id="962ae-126">System.String</span></span>

## <span data-ttu-id="962ae-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="962ae-127">OUTPUTS</span></span>

### <span data-ttu-id="962ae-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="962ae-128">System.Object</span></span>

## <span data-ttu-id="962ae-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="962ae-129">NOTES</span></span>

## <span data-ttu-id="962ae-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="962ae-130">RELATED LINKS</span></span>

