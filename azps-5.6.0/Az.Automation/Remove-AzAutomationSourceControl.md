---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: b4e60e4bbc7196736c0e49c2b294cf6cb984e7b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947544"
---
# <span data-ttu-id="b792a-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="b792a-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="b792a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b792a-102">SYNOPSIS</span></span>
<span data-ttu-id="b792a-103">Entfernt ein Azure Automation-Quellsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="b792a-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="b792a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b792a-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b792a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b792a-105">DESCRIPTION</span></span>
<span data-ttu-id="b792a-106">Das Remove-AzAutomationSourceControl-Cmdlet entfernt ein Quellsteuerelement aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b792a-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="b792a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b792a-107">EXAMPLES</span></span>

### <span data-ttu-id="b792a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b792a-108">Example 1</span></span>
<span data-ttu-id="b792a-109">Mit diesem Befehl wird das Automatisierungsquellensteuerelement mit dem Namen VSTSNative im Konto mit dem Namen devAccount entfernt.</span><span class="sxs-lookup"><span data-stu-id="b792a-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="b792a-110">Dieser Befehl gibt den Parameter *Kraft* an.</span><span class="sxs-lookup"><span data-stu-id="b792a-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="b792a-111">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b792a-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="b792a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b792a-112">PARAMETERS</span></span>

### <span data-ttu-id="b792a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b792a-113">-AutomationAccountName</span></span>
<span data-ttu-id="b792a-114">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="b792a-114">The automation account name.</span></span>

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

### <span data-ttu-id="b792a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b792a-115">-DefaultProfile</span></span>
<span data-ttu-id="b792a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b792a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b792a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b792a-117">-Name</span></span>
<span data-ttu-id="b792a-118">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="b792a-118">The source control name.</span></span>

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

### <span data-ttu-id="b792a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b792a-119">-PassThru</span></span>
<span data-ttu-id="b792a-120">PassThru gibt ein -Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b792a-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b792a-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b792a-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b792a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b792a-122">-ResourceGroupName</span></span>
<span data-ttu-id="b792a-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b792a-123">The resource group name.</span></span>

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

### <span data-ttu-id="b792a-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b792a-124">-Confirm</span></span>
<span data-ttu-id="b792a-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b792a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b792a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b792a-126">-WhatIf</span></span>
<span data-ttu-id="b792a-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b792a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b792a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b792a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b792a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b792a-129">CommonParameters</span></span>
<span data-ttu-id="b792a-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b792a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b792a-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b792a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b792a-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b792a-132">INPUTS</span></span>

### <span data-ttu-id="b792a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b792a-133">System.String</span></span>

## <span data-ttu-id="b792a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b792a-134">OUTPUTS</span></span>

### <span data-ttu-id="b792a-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="b792a-135">System.Void</span></span>

### <span data-ttu-id="b792a-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b792a-136">System.Boolean</span></span>

## <span data-ttu-id="b792a-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b792a-137">NOTES</span></span>

## <span data-ttu-id="b792a-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b792a-138">RELATED LINKS</span></span>
