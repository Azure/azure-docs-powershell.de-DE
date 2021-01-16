---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301451"
---
# <span data-ttu-id="871a9-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="871a9-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="871a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="871a9-102">SYNOPSIS</span></span>
<span data-ttu-id="871a9-103">Entfernen Sie eine Firewall.</span><span class="sxs-lookup"><span data-stu-id="871a9-103">Remove a Firewall.</span></span>

## <span data-ttu-id="871a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="871a9-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="871a9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="871a9-105">DESCRIPTION</span></span>
<span data-ttu-id="871a9-106">Das **Cmdlet "Remove-AzFirewall"** entfernt eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="871a9-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="871a9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="871a9-107">EXAMPLES</span></span>

### <span data-ttu-id="871a9-108">Beispiel 1: Erstellen und Löschen einer Firewall</span><span class="sxs-lookup"><span data-stu-id="871a9-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="871a9-109">In diesem Beispiel wird eine Firewall erstellt und dann gelöscht.</span><span class="sxs-lookup"><span data-stu-id="871a9-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="871a9-110">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen der Firewall zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="871a9-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="871a9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="871a9-111">PARAMETERS</span></span>

### <span data-ttu-id="871a9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="871a9-112">-AsJob</span></span>
<span data-ttu-id="871a9-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="871a9-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871a9-114">-DefaultProfile</span></span>
<span data-ttu-id="871a9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="871a9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="871a9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="871a9-116">-Force</span></span>
<span data-ttu-id="871a9-117">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="871a9-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871a9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="871a9-118">-Name</span></span>
<span data-ttu-id="871a9-119">Gibt den Namen der Firewall an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="871a9-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871a9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="871a9-120">-PassThru</span></span>
<span data-ttu-id="871a9-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="871a9-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="871a9-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="871a9-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="871a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="871a9-124">Gibt den Namen der Ressourcengruppe an, die die Firewall enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="871a9-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871a9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="871a9-125">-Confirm</span></span>
<span data-ttu-id="871a9-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="871a9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="871a9-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="871a9-127">-WhatIf</span></span>
<span data-ttu-id="871a9-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="871a9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="871a9-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="871a9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="871a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871a9-130">CommonParameters</span></span>
<span data-ttu-id="871a9-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871a9-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="871a9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871a9-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="871a9-133">INPUTS</span></span>

### <span data-ttu-id="871a9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="871a9-134">System.String</span></span>

## <span data-ttu-id="871a9-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="871a9-135">OUTPUTS</span></span>

### <span data-ttu-id="871a9-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="871a9-136">System.Boolean</span></span>

## <span data-ttu-id="871a9-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="871a9-137">NOTES</span></span>

## <span data-ttu-id="871a9-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="871a9-138">RELATED LINKS</span></span>

[<span data-ttu-id="871a9-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="871a9-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="871a9-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="871a9-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="871a9-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="871a9-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
