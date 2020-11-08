---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005127"
---
# <span data-ttu-id="3535f-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="3535f-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="3535f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3535f-102">SYNOPSIS</span></span>
<span data-ttu-id="3535f-103">Entfernt ein Azure Automation-Quellcodeverwaltungs-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3535f-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="3535f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3535f-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3535f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3535f-105">DESCRIPTION</span></span>
<span data-ttu-id="3535f-106">Das Remove-AzAutomationSourceControl-Cmdlet entfernt eine Quellcodeverwaltung aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="3535f-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="3535f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3535f-107">EXAMPLES</span></span>

### <span data-ttu-id="3535f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3535f-108">Example 1</span></span>
<span data-ttu-id="3535f-109">Dieser Befehl entfernt das Automatisierungs Quellen-Steuerelement mit dem Namen VSTSNative im Konto mit dem Namen devAccount.</span><span class="sxs-lookup"><span data-stu-id="3535f-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="3535f-110">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="3535f-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="3535f-111">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3535f-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="3535f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3535f-112">PARAMETERS</span></span>

### <span data-ttu-id="3535f-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3535f-113">-AutomationAccountName</span></span>
<span data-ttu-id="3535f-114">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="3535f-114">The automation account name.</span></span>

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

### <span data-ttu-id="3535f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3535f-115">-DefaultProfile</span></span>
<span data-ttu-id="3535f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3535f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3535f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3535f-117">-Name</span></span>
<span data-ttu-id="3535f-118">Der Name des Quellsteuerelements.</span><span class="sxs-lookup"><span data-stu-id="3535f-118">The source control name.</span></span>

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

### <span data-ttu-id="3535f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3535f-119">-PassThru</span></span>
<span data-ttu-id="3535f-120">PassThru gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3535f-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3535f-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3535f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3535f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3535f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3535f-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3535f-123">The resource group name.</span></span>

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

### <span data-ttu-id="3535f-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3535f-124">-Confirm</span></span>
<span data-ttu-id="3535f-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3535f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3535f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3535f-126">-WhatIf</span></span>
<span data-ttu-id="3535f-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3535f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3535f-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3535f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3535f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3535f-129">CommonParameters</span></span>
<span data-ttu-id="3535f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3535f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3535f-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3535f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3535f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3535f-132">INPUTS</span></span>

### <span data-ttu-id="3535f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3535f-133">System.String</span></span>

## <span data-ttu-id="3535f-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3535f-134">OUTPUTS</span></span>

### <span data-ttu-id="3535f-135">System. void</span><span class="sxs-lookup"><span data-stu-id="3535f-135">System.Void</span></span>

### <span data-ttu-id="3535f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3535f-136">System.Boolean</span></span>

## <span data-ttu-id="3535f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="3535f-137">NOTES</span></span>

## <span data-ttu-id="3535f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3535f-138">RELATED LINKS</span></span>
