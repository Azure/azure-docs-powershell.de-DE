---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: da9fa6503e76d9af8efbdff84ebbcdd501d8232d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840992"
---
# <span data-ttu-id="8e910-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="8e910-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="8e910-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e910-102">SYNOPSIS</span></span>
<span data-ttu-id="8e910-103">Entfernt alle AzureRm-Module von einem Computer.</span><span class="sxs-lookup"><span data-stu-id="8e910-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="8e910-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e910-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e910-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e910-105">DESCRIPTION</span></span>
<span data-ttu-id="8e910-106">Entfernt alle AzureRm-Module von einem Computer.</span><span class="sxs-lookup"><span data-stu-id="8e910-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="8e910-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e910-107">EXAMPLES</span></span>

### <span data-ttu-id="8e910-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8e910-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="8e910-109">Wenn Sie diesen Befehl ausführen, werden alle AzureRm-Module vom Computer für die Version von PowerShell entfernt, in der das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e910-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="8e910-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e910-110">PARAMETERS</span></span>

### <span data-ttu-id="8e910-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e910-111">-DefaultProfile</span></span>
<span data-ttu-id="8e910-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8e910-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e910-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e910-113">-PassThru</span></span>
<span data-ttu-id="8e910-114">Die Liste der Module, die bei Angabe entfernt wurden, wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8e910-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="8e910-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e910-115">-Confirm</span></span>
<span data-ttu-id="8e910-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e910-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e910-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e910-117">-WhatIf</span></span>
<span data-ttu-id="8e910-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e910-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e910-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e910-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e910-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e910-120">CommonParameters</span></span>
<span data-ttu-id="8e910-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e910-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e910-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e910-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e910-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e910-123">INPUTS</span></span>

### <span data-ttu-id="8e910-124">Keine</span><span class="sxs-lookup"><span data-stu-id="8e910-124">None</span></span>

## <span data-ttu-id="8e910-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e910-125">OUTPUTS</span></span>

### <span data-ttu-id="8e910-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8e910-126">System.String</span></span>

## <span data-ttu-id="8e910-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e910-127">NOTES</span></span>

## <span data-ttu-id="8e910-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e910-128">RELATED LINKS</span></span>
