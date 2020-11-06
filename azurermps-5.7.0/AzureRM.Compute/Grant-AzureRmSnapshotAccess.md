---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 8f68957020d8e4607477bd78cc42b05c29e321c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476977"
---
# <span data-ttu-id="2144c-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2144c-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="2144c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2144c-102">SYNOPSIS</span></span>
<span data-ttu-id="2144c-103">Gewährt einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="2144c-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2144c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2144c-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2144c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2144c-105">DESCRIPTION</span></span>
<span data-ttu-id="2144c-106">Das Cmdlet **Grant-AzureRmSnapshotAccess** gewährt einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="2144c-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="2144c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2144c-107">EXAMPLES</span></span>

### <span data-ttu-id="2144c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2144c-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="2144c-109">Gewähren Sie "Read"-Zugriff auf den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01" für 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="2144c-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="2144c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2144c-110">PARAMETERS</span></span>

### <span data-ttu-id="2144c-111">-Access</span><span class="sxs-lookup"><span data-stu-id="2144c-111">-Access</span></span>
<span data-ttu-id="2144c-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="2144c-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="2144c-113">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="2144c-113">-DurationInSecond</span></span>
<span data-ttu-id="2144c-114">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="2144c-114">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="2144c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2144c-115">-ResourceGroupName</span></span>
<span data-ttu-id="2144c-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2144c-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2144c-117">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="2144c-117">-SnapshotName</span></span>
<span data-ttu-id="2144c-118">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="2144c-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="2144c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2144c-119">-Confirm</span></span>
<span data-ttu-id="2144c-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2144c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2144c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2144c-121">-WhatIf</span></span>
<span data-ttu-id="2144c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2144c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2144c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2144c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2144c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2144c-124">CommonParameters</span></span>
<span data-ttu-id="2144c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2144c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2144c-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2144c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2144c-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2144c-127">INPUTS</span></span>

### <span data-ttu-id="2144c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2144c-128">System.String</span></span>

## <span data-ttu-id="2144c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2144c-129">OUTPUTS</span></span>

### <span data-ttu-id="2144c-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="2144c-130">System.Object</span></span>

## <span data-ttu-id="2144c-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2144c-131">NOTES</span></span>

## <span data-ttu-id="2144c-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2144c-132">RELATED LINKS</span></span>

