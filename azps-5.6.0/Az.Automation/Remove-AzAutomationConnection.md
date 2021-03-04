---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 0534f05bcc59a109851188c8b585badfc90d61c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947600"
---
# <span data-ttu-id="d4729-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d4729-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="d4729-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4729-102">SYNOPSIS</span></span>
<span data-ttu-id="d4729-103">Entfernt eine Automatisierungsverbindung.</span><span class="sxs-lookup"><span data-stu-id="d4729-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="d4729-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4729-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4729-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4729-105">DESCRIPTION</span></span>
<span data-ttu-id="d4729-106">Das **Cmdlet Remove-AzAutomationConnection** entfernt eine Verbindung aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d4729-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="d4729-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4729-107">EXAMPLES</span></span>

### <span data-ttu-id="d4729-108">Beispiel 1: Entfernen einer Verbindung</span><span class="sxs-lookup"><span data-stu-id="d4729-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d4729-109">Mit diesem Befehl wird ein Zertifikat namens ContosoConnection im Automatisierungskonto namens Contoso17 entfernt.</span><span class="sxs-lookup"><span data-stu-id="d4729-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d4729-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4729-110">PARAMETERS</span></span>

### <span data-ttu-id="d4729-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d4729-111">-AutomationAccountName</span></span>
<span data-ttu-id="d4729-112">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet eine Verbindung entfernt.</span><span class="sxs-lookup"><span data-stu-id="d4729-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="d4729-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4729-113">-DefaultProfile</span></span>
<span data-ttu-id="d4729-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d4729-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4729-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d4729-115">-Force</span></span>
<span data-ttu-id="d4729-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="d4729-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4729-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d4729-117">-Name</span></span>
<span data-ttu-id="d4729-118">Gibt den Namen der Verbindung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d4729-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d4729-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4729-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4729-120">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Verbindung entfernt.</span><span class="sxs-lookup"><span data-stu-id="d4729-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="d4729-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4729-121">-Confirm</span></span>
<span data-ttu-id="d4729-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4729-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4729-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4729-123">-WhatIf</span></span>
<span data-ttu-id="d4729-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4729-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4729-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4729-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4729-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4729-126">CommonParameters</span></span>
<span data-ttu-id="d4729-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4729-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4729-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4729-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4729-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4729-129">INPUTS</span></span>

### <span data-ttu-id="d4729-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d4729-130">System.String</span></span>

## <span data-ttu-id="d4729-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4729-131">OUTPUTS</span></span>

### <span data-ttu-id="d4729-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="d4729-132">System.Void</span></span>

## <span data-ttu-id="d4729-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d4729-133">NOTES</span></span>

## <span data-ttu-id="d4729-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d4729-134">RELATED LINKS</span></span>

[<span data-ttu-id="d4729-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d4729-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="d4729-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="d4729-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


