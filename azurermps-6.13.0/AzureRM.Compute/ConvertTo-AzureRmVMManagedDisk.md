---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 4aabd2a7b6e8b4b0b9037fc14189a0e14fdf8920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663004"
---
# <span data-ttu-id="8c618-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8c618-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="8c618-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c618-102">SYNOPSIS</span></span>
<span data-ttu-id="8c618-103">Wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="8c618-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c618-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c618-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c618-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c618-105">DESCRIPTION</span></span>
<span data-ttu-id="8c618-106">Das **ConvertTo-AzureRmVMManagedDisk-** Cmdlet wandelt einen virtuellen Computer mit BLOB-basierten Datenträgern auf einen virtuellen Computer mit verwalteten Datenträgern um.</span><span class="sxs-lookup"><span data-stu-id="8c618-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="8c618-107">Die Zuweisung des virtuellen Computers muss beendet werden, bevor dieser Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8c618-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="8c618-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c618-108">EXAMPLES</span></span>

### <span data-ttu-id="8c618-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c618-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="8c618-110">Dieser Befehl wandelt die BLOB-basierten Datenträger des virtuellen Computers mit dem Namen "VM01" in der Ressourcengruppe "ResourceGroup01" auf verwaltete Datenträger um.</span><span class="sxs-lookup"><span data-stu-id="8c618-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="8c618-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c618-111">PARAMETERS</span></span>

### <span data-ttu-id="8c618-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c618-112">-AsJob</span></span>
<span data-ttu-id="8c618-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8c618-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c618-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c618-114">-DefaultProfile</span></span>
<span data-ttu-id="8c618-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c618-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c618-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c618-116">-ResourceGroupName</span></span>
<span data-ttu-id="8c618-117">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8c618-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8c618-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="8c618-118">-VMName</span></span>
<span data-ttu-id="8c618-119">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="8c618-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="8c618-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c618-120">-Confirm</span></span>
<span data-ttu-id="8c618-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c618-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c618-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c618-122">-WhatIf</span></span>
<span data-ttu-id="8c618-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c618-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c618-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c618-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c618-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c618-125">CommonParameters</span></span>
<span data-ttu-id="8c618-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c618-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c618-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c618-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c618-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c618-128">INPUTS</span></span>

### <span data-ttu-id="8c618-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8c618-129">System.String</span></span>

## <span data-ttu-id="8c618-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c618-130">OUTPUTS</span></span>

### <span data-ttu-id="8c618-131">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8c618-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8c618-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c618-132">NOTES</span></span>

## <span data-ttu-id="8c618-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c618-133">RELATED LINKS</span></span>
