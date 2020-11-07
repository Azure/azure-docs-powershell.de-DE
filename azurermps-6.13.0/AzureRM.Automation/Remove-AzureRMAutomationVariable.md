---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: b336104fea097b0f5adf0993853dd6fff7bba1f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663389"
---
# <span data-ttu-id="117e4-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="117e4-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="117e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="117e4-102">SYNOPSIS</span></span>
<span data-ttu-id="117e4-103">Entfernt eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="117e4-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="117e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="117e4-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="117e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="117e4-105">DESCRIPTION</span></span>
<span data-ttu-id="117e4-106">Das Cmdlet **Remove-AzureRmAutomationVariable** entfernt eine Variable aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="117e4-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="117e4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="117e4-107">EXAMPLES</span></span>

### <span data-ttu-id="117e4-108">Beispiel 1: Entfernen einer Variablen</span><span class="sxs-lookup"><span data-stu-id="117e4-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="117e4-109">Dieser Befehl entfernt eine Variable mit dem Namen StringVariable22 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="117e4-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="117e4-110">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="117e4-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="117e4-111">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="117e4-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="117e4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="117e4-112">PARAMETERS</span></span>

### <span data-ttu-id="117e4-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="117e4-113">-AutomationAccountName</span></span>
<span data-ttu-id="117e4-114">Gibt den Namen des Automatisierungs Kontos an, das die vom Cmdlet gelöschte Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="117e4-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="117e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117e4-115">-DefaultProfile</span></span>
<span data-ttu-id="117e4-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="117e4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="117e4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="117e4-117">-Name</span></span>
<span data-ttu-id="117e4-118">Gibt den Namen der vom Cmdlet gelöschten Variablen an.</span><span class="sxs-lookup"><span data-stu-id="117e4-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117e4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117e4-119">-ResourceGroupName</span></span>
<span data-ttu-id="117e4-120">Gibt die Ressourcengruppe an, für die dieses Cmdlet eine Variable löscht.</span><span class="sxs-lookup"><span data-stu-id="117e4-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117e4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="117e4-121">-Confirm</span></span>
<span data-ttu-id="117e4-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="117e4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="117e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="117e4-123">-WhatIf</span></span>
<span data-ttu-id="117e4-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="117e4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="117e4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="117e4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="117e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117e4-126">CommonParameters</span></span>
<span data-ttu-id="117e4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117e4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117e4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117e4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="117e4-129">INPUTS</span></span>

### <span data-ttu-id="117e4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="117e4-130">System.String</span></span>

## <span data-ttu-id="117e4-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="117e4-131">OUTPUTS</span></span>

### <span data-ttu-id="117e4-132">System. void</span><span class="sxs-lookup"><span data-stu-id="117e4-132">System.Void</span></span>

## <span data-ttu-id="117e4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="117e4-133">NOTES</span></span>

## <span data-ttu-id="117e4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="117e4-134">RELATED LINKS</span></span>

[<span data-ttu-id="117e4-135">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="117e4-135">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="117e4-136">Neu – AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="117e4-136">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="117e4-137">Satz-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="117e4-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


