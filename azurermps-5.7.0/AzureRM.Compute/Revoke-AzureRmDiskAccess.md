---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503837"
---
# <span data-ttu-id="afded-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="afded-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="afded-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="afded-102">SYNOPSIS</span></span>
<span data-ttu-id="afded-103">Widerruft einen Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="afded-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afded-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="afded-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afded-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afded-105">DESCRIPTION</span></span>
<span data-ttu-id="afded-106">Mit dem Cmdlet **REVOKE-AzureRmDiskAccess** wird ein Zugriff auf einen Datenträger aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="afded-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="afded-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afded-107">EXAMPLES</span></span>

### <span data-ttu-id="afded-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afded-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="afded-109">Widerrufen des Zugriffs auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="afded-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="afded-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="afded-110">PARAMETERS</span></span>

### <span data-ttu-id="afded-111">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="afded-111">-DiskName</span></span>
<span data-ttu-id="afded-112">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="afded-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="afded-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afded-113">-ResourceGroupName</span></span>
<span data-ttu-id="afded-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="afded-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="afded-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="afded-115">-Confirm</span></span>
<span data-ttu-id="afded-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afded-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afded-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afded-117">-WhatIf</span></span>
<span data-ttu-id="afded-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afded-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afded-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afded-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afded-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afded-120">CommonParameters</span></span>
<span data-ttu-id="afded-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afded-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afded-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afded-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afded-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="afded-123">INPUTS</span></span>

### <span data-ttu-id="afded-124">System. String</span><span class="sxs-lookup"><span data-stu-id="afded-124">System.String</span></span>

## <span data-ttu-id="afded-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="afded-125">OUTPUTS</span></span>

### <span data-ttu-id="afded-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="afded-126">System.Object</span></span>

## <span data-ttu-id="afded-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="afded-127">NOTES</span></span>

## <span data-ttu-id="afded-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="afded-128">RELATED LINKS</span></span>

