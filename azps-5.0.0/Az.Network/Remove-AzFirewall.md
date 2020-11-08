---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179843"
---
# <span data-ttu-id="96307-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96307-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="96307-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96307-102">SYNOPSIS</span></span>
<span data-ttu-id="96307-103">Entfernen Sie eine Firewall.</span><span class="sxs-lookup"><span data-stu-id="96307-103">Remove a Firewall.</span></span>

## <span data-ttu-id="96307-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96307-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96307-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96307-105">DESCRIPTION</span></span>
<span data-ttu-id="96307-106">Das Cmdlet **Remove-AzFirewall** entfernt eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="96307-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="96307-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96307-107">EXAMPLES</span></span>

### <span data-ttu-id="96307-108">Beispiel 1: Erstellen und Löschen einer Firewall</span><span class="sxs-lookup"><span data-stu-id="96307-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="96307-109">In diesem Beispiel wird eine Firewall erstellt und dann gelöscht.</span><span class="sxs-lookup"><span data-stu-id="96307-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="96307-110">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen der Firewall zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="96307-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="96307-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="96307-111">PARAMETERS</span></span>

### <span data-ttu-id="96307-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96307-112">-AsJob</span></span>
<span data-ttu-id="96307-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="96307-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96307-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96307-114">-DefaultProfile</span></span>
<span data-ttu-id="96307-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="96307-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96307-116">-Force</span><span class="sxs-lookup"><span data-stu-id="96307-116">-Force</span></span>
<span data-ttu-id="96307-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="96307-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="96307-118">-Name</span><span class="sxs-lookup"><span data-stu-id="96307-118">-Name</span></span>
<span data-ttu-id="96307-119">Gibt den Namen der Firewall an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="96307-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96307-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96307-120">-PassThru</span></span>
<span data-ttu-id="96307-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="96307-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="96307-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="96307-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="96307-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96307-123">-ResourceGroupName</span></span>
<span data-ttu-id="96307-124">Gibt den Namen der Ressourcengruppe an, die die vom Cmdlet entfernte Firewall enthält.</span><span class="sxs-lookup"><span data-stu-id="96307-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="96307-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96307-125">-Confirm</span></span>
<span data-ttu-id="96307-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96307-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96307-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96307-127">-WhatIf</span></span>
<span data-ttu-id="96307-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96307-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96307-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96307-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96307-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96307-130">CommonParameters</span></span>
<span data-ttu-id="96307-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96307-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96307-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96307-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96307-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96307-133">INPUTS</span></span>

### <span data-ttu-id="96307-134">System. String</span><span class="sxs-lookup"><span data-stu-id="96307-134">System.String</span></span>

## <span data-ttu-id="96307-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96307-135">OUTPUTS</span></span>

### <span data-ttu-id="96307-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96307-136">System.Boolean</span></span>

## <span data-ttu-id="96307-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="96307-137">NOTES</span></span>

## <span data-ttu-id="96307-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96307-138">RELATED LINKS</span></span>

[<span data-ttu-id="96307-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96307-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="96307-140">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96307-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="96307-141">Satz-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="96307-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
