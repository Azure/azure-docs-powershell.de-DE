---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: d2e495b58e68232bf20bd309d06207cd45cd427e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658428"
---
# <span data-ttu-id="2525d-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="2525d-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="2525d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2525d-102">SYNOPSIS</span></span>
<span data-ttu-id="2525d-103">Entfernt alle AzureRm-Module von einem Computer.</span><span class="sxs-lookup"><span data-stu-id="2525d-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="2525d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2525d-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2525d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2525d-105">DESCRIPTION</span></span>
<span data-ttu-id="2525d-106">Entfernt alle AzureRm-Module von einem Computer.</span><span class="sxs-lookup"><span data-stu-id="2525d-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="2525d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2525d-107">EXAMPLES</span></span>

### <span data-ttu-id="2525d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2525d-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="2525d-109">Wenn Sie diesen Befehl ausführen, werden alle AzureRm-Module vom Computer für die Version von PowerShell entfernt, in der das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2525d-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="2525d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2525d-110">PARAMETERS</span></span>

### <span data-ttu-id="2525d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2525d-111">-DefaultProfile</span></span>
<span data-ttu-id="2525d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2525d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2525d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2525d-113">-PassThru</span></span>
<span data-ttu-id="2525d-114">Die Liste der Module, die bei Angabe entfernt wurden, wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2525d-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="2525d-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2525d-115">-Confirm</span></span>
<span data-ttu-id="2525d-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2525d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2525d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2525d-117">-WhatIf</span></span>
<span data-ttu-id="2525d-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2525d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2525d-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2525d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2525d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2525d-120">CommonParameters</span></span>
<span data-ttu-id="2525d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2525d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2525d-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2525d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2525d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2525d-123">INPUTS</span></span>

### <span data-ttu-id="2525d-124">Keine</span><span class="sxs-lookup"><span data-stu-id="2525d-124">None</span></span>

## <span data-ttu-id="2525d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2525d-125">OUTPUTS</span></span>

### <span data-ttu-id="2525d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2525d-126">System.String</span></span>

## <span data-ttu-id="2525d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="2525d-127">NOTES</span></span>

## <span data-ttu-id="2525d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2525d-128">RELATED LINKS</span></span>
