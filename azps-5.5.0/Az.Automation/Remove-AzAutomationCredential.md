---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171695"
---
# <span data-ttu-id="d8c72-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d8c72-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="d8c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c72-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c72-103">Entfernt die Anmeldeinformationen für die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="d8c72-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="d8c72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8c72-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c72-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8c72-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c72-106">Das **Cmdlet "Remove-AzAutomationCredential"** entfernt Anmeldeinformationen aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="d8c72-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="d8c72-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d8c72-107">EXAMPLES</span></span>

### <span data-ttu-id="d8c72-108">Beispiel 1: Entfernen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="d8c72-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d8c72-109">Mit diesem Befehl werden die Anmeldeinformationen "ContosoCredential" im Azure -Automatisierungskonto namens "Contoso17" entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8c72-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d8c72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8c72-110">PARAMETERS</span></span>

### <span data-ttu-id="d8c72-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8c72-111">-AutomationAccountName</span></span>
<span data-ttu-id="d8c72-112">Gibt den Namen des Automatisierungskontos an, aus dem dieses Cmdlet Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8c72-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="d8c72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c72-113">-DefaultProfile</span></span>
<span data-ttu-id="d8c72-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d8c72-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8c72-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d8c72-115">-Name</span></span>
<span data-ttu-id="d8c72-116">Gibt den Namen der Anmeldeinformationen an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d8c72-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d8c72-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8c72-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8c72-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen entfernt.</span><span class="sxs-lookup"><span data-stu-id="d8c72-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="d8c72-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8c72-119">-Confirm</span></span>
<span data-ttu-id="d8c72-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d8c72-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c72-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d8c72-121">-WhatIf</span></span>
<span data-ttu-id="d8c72-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8c72-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c72-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d8c72-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c72-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c72-124">CommonParameters</span></span>
<span data-ttu-id="d8c72-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8c72-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c72-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c72-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c72-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d8c72-127">INPUTS</span></span>

### <span data-ttu-id="d8c72-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d8c72-128">System.String</span></span>

## <span data-ttu-id="d8c72-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d8c72-129">OUTPUTS</span></span>

### <span data-ttu-id="d8c72-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d8c72-130">System.Void</span></span>

## <span data-ttu-id="d8c72-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d8c72-131">NOTES</span></span>

## <span data-ttu-id="d8c72-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d8c72-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8c72-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d8c72-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="d8c72-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d8c72-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="d8c72-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="d8c72-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


