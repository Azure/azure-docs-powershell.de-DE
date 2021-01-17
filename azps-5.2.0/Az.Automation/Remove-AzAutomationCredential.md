---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373328"
---
# <span data-ttu-id="460d9-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="460d9-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="460d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="460d9-102">SYNOPSIS</span></span>
<span data-ttu-id="460d9-103">Entfernt die Anmeldeinformationen für die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="460d9-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="460d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="460d9-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="460d9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="460d9-105">DESCRIPTION</span></span>
<span data-ttu-id="460d9-106">Das **Cmdlet "Remove-AzAutomationCredential"** entfernt Anmeldeinformationen aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="460d9-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="460d9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="460d9-107">EXAMPLES</span></span>

### <span data-ttu-id="460d9-108">Beispiel 1: Entfernen einer Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="460d9-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="460d9-109">Mit diesem Befehl werden die Anmeldeinformationen "ContosoCredential" im Azure -Automatisierungskonto namens "Contoso17" entfernt.</span><span class="sxs-lookup"><span data-stu-id="460d9-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="460d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="460d9-110">PARAMETERS</span></span>

### <span data-ttu-id="460d9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="460d9-111">-AutomationAccountName</span></span>
<span data-ttu-id="460d9-112">Gibt den Namen des Automatisierungskontos an, aus dem dieses Cmdlet Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="460d9-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="460d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460d9-113">-DefaultProfile</span></span>
<span data-ttu-id="460d9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="460d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="460d9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="460d9-115">-Name</span></span>
<span data-ttu-id="460d9-116">Gibt den Namen der Anmeldeinformationen an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="460d9-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="460d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="460d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="460d9-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="460d9-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="460d9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="460d9-119">-Confirm</span></span>
<span data-ttu-id="460d9-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="460d9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="460d9-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="460d9-121">-WhatIf</span></span>
<span data-ttu-id="460d9-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="460d9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="460d9-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="460d9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="460d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460d9-124">CommonParameters</span></span>
<span data-ttu-id="460d9-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="460d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460d9-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="460d9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460d9-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="460d9-127">INPUTS</span></span>

### <span data-ttu-id="460d9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="460d9-128">System.String</span></span>

## <span data-ttu-id="460d9-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="460d9-129">OUTPUTS</span></span>

### <span data-ttu-id="460d9-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="460d9-130">System.Void</span></span>

## <span data-ttu-id="460d9-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="460d9-131">NOTES</span></span>

## <span data-ttu-id="460d9-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="460d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="460d9-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="460d9-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="460d9-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="460d9-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="460d9-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="460d9-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


