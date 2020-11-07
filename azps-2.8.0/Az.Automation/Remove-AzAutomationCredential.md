---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 703be26244e61b797f3359ef508d92e38847bf8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657974"
---
# <span data-ttu-id="93e69-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="93e69-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="93e69-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93e69-102">SYNOPSIS</span></span>
<span data-ttu-id="93e69-103">Entfernt eine Automatisierungs Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="93e69-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="93e69-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93e69-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e69-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93e69-105">DESCRIPTION</span></span>
<span data-ttu-id="93e69-106">Mit dem Cmdlet **Remove-AzAutomationCredential** werden Anmeldeinformationen aus Azure Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="93e69-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="93e69-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93e69-107">EXAMPLES</span></span>

### <span data-ttu-id="93e69-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="93e69-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="93e69-109">Dieser Befehl entfernt die Anmeldeinformationen mit dem Namen ContosoCredential im Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="93e69-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="93e69-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93e69-110">PARAMETERS</span></span>

### <span data-ttu-id="93e69-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="93e69-111">-AutomationAccountName</span></span>
<span data-ttu-id="93e69-112">Gibt den Namen des Automatisierungs Kontos an, aus dem dieses Cmdlet eine Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="93e69-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="93e69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e69-113">-DefaultProfile</span></span>
<span data-ttu-id="93e69-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="93e69-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93e69-115">-Name</span><span class="sxs-lookup"><span data-stu-id="93e69-115">-Name</span></span>
<span data-ttu-id="93e69-116">Gibt den Namen der Anmeldeinformationen an, die vom Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="93e69-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="93e69-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e69-117">-ResourceGroupName</span></span>
<span data-ttu-id="93e69-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="93e69-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="93e69-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93e69-119">-Confirm</span></span>
<span data-ttu-id="93e69-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93e69-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e69-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e69-121">-WhatIf</span></span>
<span data-ttu-id="93e69-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93e69-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e69-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93e69-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e69-124">CommonParameters</span></span>
<span data-ttu-id="93e69-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e69-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e69-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e69-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93e69-127">INPUTS</span></span>

### <span data-ttu-id="93e69-128">System. String</span><span class="sxs-lookup"><span data-stu-id="93e69-128">System.String</span></span>

## <span data-ttu-id="93e69-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93e69-129">OUTPUTS</span></span>

### <span data-ttu-id="93e69-130">System. void</span><span class="sxs-lookup"><span data-stu-id="93e69-130">System.Void</span></span>

## <span data-ttu-id="93e69-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="93e69-131">NOTES</span></span>

## <span data-ttu-id="93e69-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93e69-132">RELATED LINKS</span></span>

[<span data-ttu-id="93e69-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="93e69-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="93e69-134">Neu – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="93e69-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="93e69-135">Satz-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="93e69-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


