---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 30029a6fbd14a7e94ffe60f058405a2907b1cb53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480445"
---
# <span data-ttu-id="c0aea-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c0aea-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="c0aea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0aea-102">SYNOPSIS</span></span>
<span data-ttu-id="c0aea-103">Entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c0aea-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0aea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0aea-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0aea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0aea-105">DESCRIPTION</span></span>
<span data-ttu-id="c0aea-106">Das Cmdlet **Remove-AzureRmDisk** entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c0aea-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="c0aea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0aea-107">EXAMPLES</span></span>

### <span data-ttu-id="c0aea-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0aea-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="c0aea-109">Dieser Befehl entfernt den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c0aea-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c0aea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0aea-110">PARAMETERS</span></span>

### <span data-ttu-id="c0aea-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0aea-111">-AsJob</span></span>
<span data-ttu-id="c0aea-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="c0aea-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c0aea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0aea-113">-DefaultProfile</span></span>
<span data-ttu-id="c0aea-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0aea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0aea-115">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="c0aea-115">-DiskName</span></span>
<span data-ttu-id="c0aea-116">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="c0aea-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="c0aea-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c0aea-117">-Force</span></span>
<span data-ttu-id="c0aea-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c0aea-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0aea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0aea-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0aea-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c0aea-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c0aea-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0aea-121">-Confirm</span></span>
<span data-ttu-id="c0aea-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0aea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0aea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0aea-123">-WhatIf</span></span>
<span data-ttu-id="c0aea-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0aea-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0aea-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0aea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0aea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0aea-126">CommonParameters</span></span>
<span data-ttu-id="c0aea-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0aea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0aea-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0aea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0aea-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0aea-129">INPUTS</span></span>

### <span data-ttu-id="c0aea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c0aea-130">System.String</span></span>

## <span data-ttu-id="c0aea-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0aea-131">OUTPUTS</span></span>

### <span data-ttu-id="c0aea-132">Microsoft. Azure. Commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c0aea-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c0aea-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0aea-133">NOTES</span></span>

## <span data-ttu-id="c0aea-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0aea-134">RELATED LINKS</span></span>
