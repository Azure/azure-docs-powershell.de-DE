---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: dea9f62583cca8f3a5ee9ce05b6b7e60e8bf4755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496653"
---
# <span data-ttu-id="87a98-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="87a98-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="87a98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87a98-102">SYNOPSIS</span></span>
<span data-ttu-id="87a98-103">Entfernt eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="87a98-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87a98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87a98-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87a98-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87a98-105">DESCRIPTION</span></span>
<span data-ttu-id="87a98-106">Das Cmdlet **Remove-AzureRmAutomationVariable** entfernt eine Variable aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="87a98-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="87a98-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87a98-107">EXAMPLES</span></span>

### <span data-ttu-id="87a98-108">Beispiel 1: Entfernen einer Variablen</span><span class="sxs-lookup"><span data-stu-id="87a98-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="87a98-109">Dieser Befehl entfernt eine Variable mit dem Namen StringVariable22 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="87a98-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="87a98-110">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="87a98-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="87a98-111">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="87a98-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="87a98-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="87a98-112">PARAMETERS</span></span>

### <span data-ttu-id="87a98-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87a98-113">-AutomationAccountName</span></span>
<span data-ttu-id="87a98-114">Gibt den Namen des Automatisierungs Kontos an, das die vom Cmdlet gelöschte Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="87a98-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="87a98-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a98-115">-DefaultProfile</span></span>
<span data-ttu-id="87a98-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="87a98-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a98-117">-Name</span><span class="sxs-lookup"><span data-stu-id="87a98-117">-Name</span></span>
<span data-ttu-id="87a98-118">Gibt den Namen der vom Cmdlet gelöschten Variablen an.</span><span class="sxs-lookup"><span data-stu-id="87a98-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a98-119">-ResourceGroupName</span></span>
<span data-ttu-id="87a98-120">Gibt die Ressourcengruppe an, für die dieses Cmdlet eine Variable löscht.</span><span class="sxs-lookup"><span data-stu-id="87a98-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87a98-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87a98-121">-Confirm</span></span>
<span data-ttu-id="87a98-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87a98-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a98-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a98-123">-WhatIf</span></span>
<span data-ttu-id="87a98-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87a98-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87a98-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87a98-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a98-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a98-126">CommonParameters</span></span>
<span data-ttu-id="87a98-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a98-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a98-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a98-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a98-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87a98-129">INPUTS</span></span>

### <span data-ttu-id="87a98-130">Keine</span><span class="sxs-lookup"><span data-stu-id="87a98-130">None</span></span>
<span data-ttu-id="87a98-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="87a98-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87a98-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87a98-132">OUTPUTS</span></span>

### <span data-ttu-id="87a98-133">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="87a98-133">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="87a98-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="87a98-134">NOTES</span></span>

## <span data-ttu-id="87a98-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87a98-135">RELATED LINKS</span></span>

[<span data-ttu-id="87a98-136">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="87a98-136">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="87a98-137">Neu – AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="87a98-137">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="87a98-138">Satz-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="87a98-138">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


