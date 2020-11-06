---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 6931f6d80d3e279259b599b782a505b2a21dd074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505198"
---
# <span data-ttu-id="b5f3e-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b5f3e-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="b5f3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f3e-103">Wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5f3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5f3e-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5f3e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="b5f3e-106">Das **ConvertTo-AzureRmVMManagedDisk-** Cmdlet wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="b5f3e-107">Die Zuweisung des virtuellen Computers muss beendet werden, bevor dieser Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="b5f3e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5f3e-108">EXAMPLES</span></span>

### <span data-ttu-id="b5f3e-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b5f3e-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="b5f3e-110">Dieser Befehl wandelt die BLOB-basierten Datenträger des virtuellen Computers mit dem Namen "VM01" in der Ressourcengruppe "ResourceGroup01" auf verwaltete Datenträger um.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="b5f3e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5f3e-111">PARAMETERS</span></span>

### <span data-ttu-id="b5f3e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f3e-112">-DefaultProfile</span></span>
<span data-ttu-id="b5f3e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5f3e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5f3e-114">-ResourceGroupName</span></span>
<span data-ttu-id="b5f3e-115">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-115">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3e-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="b5f3e-116">-VMName</span></span>
<span data-ttu-id="b5f3e-117">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f3e-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5f3e-118">-Confirm</span></span>
<span data-ttu-id="b5f3e-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5f3e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5f3e-120">-WhatIf</span></span>
<span data-ttu-id="b5f3e-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5f3e-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5f3e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f3e-123">CommonParameters</span></span>
<span data-ttu-id="b5f3e-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5f3e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f3e-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f3e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f3e-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5f3e-126">INPUTS</span></span>

### <span data-ttu-id="b5f3e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b5f3e-127">System.String</span></span>

## <span data-ttu-id="b5f3e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5f3e-128">OUTPUTS</span></span>

### <span data-ttu-id="b5f3e-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="b5f3e-129">System.Object</span></span>

## <span data-ttu-id="b5f3e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5f3e-130">NOTES</span></span>

## <span data-ttu-id="b5f3e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5f3e-131">RELATED LINKS</span></span>

