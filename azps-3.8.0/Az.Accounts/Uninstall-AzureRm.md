---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996689"
---
# <span data-ttu-id="6b4d4-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="6b4d4-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="6b4d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="6b4d4-103">Entfernt alle AzureRm-Module von einem Computer.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="6b4d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b4d4-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b4d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b4d4-105">DESCRIPTION</span></span>
<span data-ttu-id="6b4d4-106">Entfernt alle AzureRm-Module von einem Computer.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="6b4d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b4d4-107">EXAMPLES</span></span>

### <span data-ttu-id="6b4d4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b4d4-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="6b4d4-109">Wenn Sie diesen Befehl ausführen, werden alle AzureRm-Module vom Computer für die Version von PowerShell entfernt, in der das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="6b4d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b4d4-110">PARAMETERS</span></span>

### <span data-ttu-id="6b4d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b4d4-111">-DefaultProfile</span></span>
<span data-ttu-id="6b4d4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b4d4-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b4d4-113">-PassThru</span></span>
<span data-ttu-id="6b4d4-114">Die Liste der Module, die bei Angabe entfernt wurden, wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="6b4d4-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b4d4-115">-Confirm</span></span>
<span data-ttu-id="6b4d4-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b4d4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b4d4-117">-WhatIf</span></span>
<span data-ttu-id="6b4d4-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b4d4-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b4d4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b4d4-120">CommonParameters</span></span>
<span data-ttu-id="6b4d4-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b4d4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b4d4-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b4d4-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b4d4-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b4d4-123">INPUTS</span></span>

### <span data-ttu-id="6b4d4-124">Keine</span><span class="sxs-lookup"><span data-stu-id="6b4d4-124">None</span></span>

## <span data-ttu-id="6b4d4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b4d4-125">OUTPUTS</span></span>

### <span data-ttu-id="6b4d4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6b4d4-126">System.String</span></span>

## <span data-ttu-id="6b4d4-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b4d4-127">NOTES</span></span>

## <span data-ttu-id="6b4d4-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b4d4-128">RELATED LINKS</span></span>
