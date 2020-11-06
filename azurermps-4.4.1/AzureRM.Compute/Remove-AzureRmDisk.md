---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: bcfba4bb002d7982f9a0fb9220fbce24e12e6ffb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505150"
---
# <span data-ttu-id="aaff0-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="aaff0-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="aaff0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aaff0-102">SYNOPSIS</span></span>
<span data-ttu-id="aaff0-103">Entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="aaff0-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaff0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaff0-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaff0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aaff0-105">DESCRIPTION</span></span>
<span data-ttu-id="aaff0-106">Das Cmdlet **Remove-AzureRmDisk** entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="aaff0-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="aaff0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aaff0-107">EXAMPLES</span></span>

### <span data-ttu-id="aaff0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aaff0-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="aaff0-109">Dieser Befehl entfernt den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="aaff0-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="aaff0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aaff0-110">PARAMETERS</span></span>

### <span data-ttu-id="aaff0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaff0-111">-DefaultProfile</span></span>
<span data-ttu-id="aaff0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aaff0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaff0-113">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="aaff0-113">-DiskName</span></span>
<span data-ttu-id="aaff0-114">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="aaff0-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="aaff0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aaff0-115">-Force</span></span>
<span data-ttu-id="aaff0-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="aaff0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aaff0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaff0-117">-ResourceGroupName</span></span>
<span data-ttu-id="aaff0-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="aaff0-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aaff0-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aaff0-119">-Confirm</span></span>
<span data-ttu-id="aaff0-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aaff0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaff0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaff0-121">-WhatIf</span></span>
<span data-ttu-id="aaff0-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aaff0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaff0-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aaff0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaff0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaff0-124">CommonParameters</span></span>
<span data-ttu-id="aaff0-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaff0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaff0-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaff0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaff0-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aaff0-127">INPUTS</span></span>

### <span data-ttu-id="aaff0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="aaff0-128">System.String</span></span>

## <span data-ttu-id="aaff0-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aaff0-129">OUTPUTS</span></span>

### <span data-ttu-id="aaff0-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="aaff0-130">System.Object</span></span>

## <span data-ttu-id="aaff0-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="aaff0-131">NOTES</span></span>

## <span data-ttu-id="aaff0-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aaff0-132">RELATED LINKS</span></span>

