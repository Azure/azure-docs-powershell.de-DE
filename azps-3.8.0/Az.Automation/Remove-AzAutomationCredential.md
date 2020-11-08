---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005141"
---
# <span data-ttu-id="9ab79-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9ab79-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="9ab79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ab79-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab79-103">Entfernt eine Automatisierungs Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="9ab79-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="9ab79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ab79-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ab79-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ab79-105">DESCRIPTION</span></span>
<span data-ttu-id="9ab79-106">Mit dem Cmdlet **Remove-AzAutomationCredential** werden Anmeldeinformationen aus Azure Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="9ab79-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="9ab79-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ab79-107">EXAMPLES</span></span>

### <span data-ttu-id="9ab79-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="9ab79-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9ab79-109">Dieser Befehl entfernt die Anmeldeinformationen mit dem Namen ContosoCredential im Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ab79-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9ab79-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ab79-110">PARAMETERS</span></span>

### <span data-ttu-id="9ab79-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9ab79-111">-AutomationAccountName</span></span>
<span data-ttu-id="9ab79-112">Gibt den Namen des Automatisierungs Kontos an, aus dem dieses Cmdlet eine Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="9ab79-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="9ab79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab79-113">-DefaultProfile</span></span>
<span data-ttu-id="9ab79-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9ab79-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ab79-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9ab79-115">-Name</span></span>
<span data-ttu-id="9ab79-116">Gibt den Namen der Anmeldeinformationen an, die vom Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9ab79-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9ab79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab79-117">-ResourceGroupName</span></span>
<span data-ttu-id="9ab79-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="9ab79-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="9ab79-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ab79-119">-Confirm</span></span>
<span data-ttu-id="9ab79-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ab79-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab79-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab79-121">-WhatIf</span></span>
<span data-ttu-id="9ab79-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ab79-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ab79-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ab79-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab79-124">CommonParameters</span></span>
<span data-ttu-id="9ab79-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab79-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab79-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab79-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ab79-127">INPUTS</span></span>

### <span data-ttu-id="9ab79-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9ab79-128">System.String</span></span>

## <span data-ttu-id="9ab79-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ab79-129">OUTPUTS</span></span>

### <span data-ttu-id="9ab79-130">System. void</span><span class="sxs-lookup"><span data-stu-id="9ab79-130">System.Void</span></span>

## <span data-ttu-id="9ab79-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ab79-131">NOTES</span></span>

## <span data-ttu-id="9ab79-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ab79-132">RELATED LINKS</span></span>

[<span data-ttu-id="9ab79-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9ab79-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="9ab79-134">Neu – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9ab79-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="9ab79-135">Satz-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="9ab79-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


