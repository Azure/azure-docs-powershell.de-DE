---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471262"
---
# <span data-ttu-id="fe172-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="fe172-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="fe172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe172-102">SYNOPSIS</span></span>
<span data-ttu-id="fe172-103">Entfernt ein Azure Automation-Quellsteuerelement.</span><span class="sxs-lookup"><span data-stu-id="fe172-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="fe172-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe172-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe172-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe172-105">DESCRIPTION</span></span>
<span data-ttu-id="fe172-106">Das Remove-AzAutomationSourceControl entfernt ein Quellsteuerelement aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="fe172-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="fe172-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fe172-107">EXAMPLES</span></span>

### <span data-ttu-id="fe172-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fe172-108">Example 1</span></span>
<span data-ttu-id="fe172-109">Mit diesem Befehl wird das Automatisierungsquellensteuerelement namens VSTSNative im Konto mit dem Namen "devAccount" entfernt.</span><span class="sxs-lookup"><span data-stu-id="fe172-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="fe172-110">Dieser Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="fe172-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="fe172-111">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="fe172-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="fe172-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe172-112">PARAMETERS</span></span>

### <span data-ttu-id="fe172-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fe172-113">-AutomationAccountName</span></span>
<span data-ttu-id="fe172-114">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="fe172-114">The automation account name.</span></span>

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

### <span data-ttu-id="fe172-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe172-115">-DefaultProfile</span></span>
<span data-ttu-id="fe172-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fe172-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe172-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fe172-117">-Name</span></span>
<span data-ttu-id="fe172-118">Der Name des Quellcodeverwaltungssteuerelements.</span><span class="sxs-lookup"><span data-stu-id="fe172-118">The source control name.</span></span>

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

### <span data-ttu-id="fe172-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe172-119">-PassThru</span></span>
<span data-ttu-id="fe172-120">PassThru gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fe172-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fe172-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="fe172-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe172-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe172-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe172-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fe172-123">The resource group name.</span></span>

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

### <span data-ttu-id="fe172-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe172-124">-Confirm</span></span>
<span data-ttu-id="fe172-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fe172-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe172-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fe172-126">-WhatIf</span></span>
<span data-ttu-id="fe172-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fe172-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe172-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe172-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe172-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe172-129">CommonParameters</span></span>
<span data-ttu-id="fe172-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe172-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe172-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe172-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe172-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fe172-132">INPUTS</span></span>

### <span data-ttu-id="fe172-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fe172-133">System.String</span></span>

## <span data-ttu-id="fe172-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fe172-134">OUTPUTS</span></span>

### <span data-ttu-id="fe172-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="fe172-135">System.Void</span></span>

### <span data-ttu-id="fe172-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe172-136">System.Boolean</span></span>

## <span data-ttu-id="fe172-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fe172-137">NOTES</span></span>

## <span data-ttu-id="fe172-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fe172-138">RELATED LINKS</span></span>
