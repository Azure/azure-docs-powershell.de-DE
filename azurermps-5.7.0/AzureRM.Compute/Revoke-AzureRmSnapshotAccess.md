---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664674"
---
# <span data-ttu-id="ed261-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ed261-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="ed261-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed261-102">SYNOPSIS</span></span>
<span data-ttu-id="ed261-103">Widerruft einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="ed261-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed261-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed261-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed261-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed261-105">DESCRIPTION</span></span>
<span data-ttu-id="ed261-106">Das **REVOKE-AzureRmSnapshotAccess-** Cmdlet widerruft einen Zugriff auf einen Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="ed261-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="ed261-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed261-107">EXAMPLES</span></span>

### <span data-ttu-id="ed261-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ed261-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="ed261-109">Widerrufen des Zugriffs auf den Snapshot mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="ed261-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="ed261-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed261-110">PARAMETERS</span></span>

### <span data-ttu-id="ed261-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed261-111">-ResourceGroupName</span></span>
<span data-ttu-id="ed261-112">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed261-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ed261-113">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="ed261-113">-SnapshotName</span></span>
<span data-ttu-id="ed261-114">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="ed261-114">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="ed261-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed261-115">-Confirm</span></span>
<span data-ttu-id="ed261-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed261-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed261-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed261-117">-WhatIf</span></span>
<span data-ttu-id="ed261-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed261-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed261-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed261-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed261-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed261-120">CommonParameters</span></span>
<span data-ttu-id="ed261-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed261-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed261-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed261-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed261-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed261-123">INPUTS</span></span>

### <span data-ttu-id="ed261-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ed261-124">System.String</span></span>

## <span data-ttu-id="ed261-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed261-125">OUTPUTS</span></span>

### <span data-ttu-id="ed261-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="ed261-126">System.Object</span></span>

## <span data-ttu-id="ed261-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed261-127">NOTES</span></span>

## <span data-ttu-id="ed261-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed261-128">RELATED LINKS</span></span>

