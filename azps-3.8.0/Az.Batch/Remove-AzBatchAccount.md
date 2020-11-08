---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 2dc76b09a48b3e34f01378405437f39782df56f0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007416"
---
# <span data-ttu-id="83cb2-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="83cb2-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="83cb2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="83cb2-103">Entfernt ein Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="83cb2-103">Removes a Batch account.</span></span>

## <span data-ttu-id="83cb2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83cb2-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83cb2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83cb2-105">DESCRIPTION</span></span>
<span data-ttu-id="83cb2-106">Das Cmdlet **Remove-AzBatchAccount** entfernt ein Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="83cb2-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="83cb2-107">Dieses Cmdlet fordert Sie auf, bevor ein Konto entfernt wird, es sei denn, Sie geben den Parameter *Force* an.</span><span class="sxs-lookup"><span data-stu-id="83cb2-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="83cb2-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83cb2-108">EXAMPLES</span></span>

### <span data-ttu-id="83cb2-109">Beispiel 1: Entfernen eines Stapelverarbeitungs Kontos</span><span class="sxs-lookup"><span data-stu-id="83cb2-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="83cb2-110">Dieser Befehl entfernt das Batch Konto mit dem Namen pfuller.</span><span class="sxs-lookup"><span data-stu-id="83cb2-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="83cb2-111">Mit diesem Befehl werden Sie zur Bestätigung aufgefordert, bevor Sie das Konto löschen.</span><span class="sxs-lookup"><span data-stu-id="83cb2-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="83cb2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="83cb2-112">PARAMETERS</span></span>

### <span data-ttu-id="83cb2-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="83cb2-113">-AccountName</span></span>
<span data-ttu-id="83cb2-114">Gibt den Namen des Batch Kontos an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="83cb2-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83cb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83cb2-115">-DefaultProfile</span></span>
<span data-ttu-id="83cb2-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83cb2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cb2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="83cb2-117">-Force</span></span>
<span data-ttu-id="83cb2-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="83cb2-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="83cb2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83cb2-119">-ResourceGroupName</span></span>
<span data-ttu-id="83cb2-120">Gibt die Ressourcengruppe des Kontos an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="83cb2-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83cb2-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="83cb2-121">-Confirm</span></span>
<span data-ttu-id="83cb2-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="83cb2-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cb2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83cb2-123">-WhatIf</span></span>
<span data-ttu-id="83cb2-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="83cb2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83cb2-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="83cb2-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83cb2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83cb2-126">CommonParameters</span></span>
<span data-ttu-id="83cb2-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83cb2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83cb2-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83cb2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83cb2-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83cb2-129">INPUTS</span></span>

### <span data-ttu-id="83cb2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="83cb2-130">System.String</span></span>

## <span data-ttu-id="83cb2-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83cb2-131">OUTPUTS</span></span>

### <span data-ttu-id="83cb2-132">System. void</span><span class="sxs-lookup"><span data-stu-id="83cb2-132">System.Void</span></span>

## <span data-ttu-id="83cb2-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="83cb2-133">NOTES</span></span>

## <span data-ttu-id="83cb2-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83cb2-134">RELATED LINKS</span></span>

[<span data-ttu-id="83cb2-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="83cb2-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="83cb2-136">Neu – AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="83cb2-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="83cb2-137">Satz-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="83cb2-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="83cb2-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="83cb2-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


