---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: b46540a614f25a3923301e28cd19d8f1b76af53c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660372"
---
# <span data-ttu-id="12aeb-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="12aeb-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="12aeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="12aeb-103">Entfernen Sie eine Firewall.</span><span class="sxs-lookup"><span data-stu-id="12aeb-103">Remove a Firewall.</span></span>

## <span data-ttu-id="12aeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12aeb-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12aeb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12aeb-105">DESCRIPTION</span></span>
<span data-ttu-id="12aeb-106">Das Cmdlet **Remove-AzFirewall** entfernt eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="12aeb-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="12aeb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12aeb-107">EXAMPLES</span></span>

### <span data-ttu-id="12aeb-108">1: Erstellen und Löschen einer Firewall</span><span class="sxs-lookup"><span data-stu-id="12aeb-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="12aeb-109">In diesem Beispiel wird eine Firewall erstellt und dann gelöscht.</span><span class="sxs-lookup"><span data-stu-id="12aeb-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="12aeb-110">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen der Firewall zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="12aeb-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="12aeb-111">2: Freigeben der Firewall und anschließendes Löschen der Firewall</span><span class="sxs-lookup"><span data-stu-id="12aeb-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="12aeb-112">In diesem Beispiel wird eine Firewall abgerufen, die Firewall dereserviert und dann die Firewall gelöscht.</span><span class="sxs-lookup"><span data-stu-id="12aeb-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="12aeb-113">Mit dem Befehl "freigeben" wird der ausgeführte Dienst entfernt, die Konfiguration der Firewall bleibt jedoch erhalten.</span><span class="sxs-lookup"><span data-stu-id="12aeb-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="12aeb-114">Wenn der Benutzer den Dienst erneut starten möchte, sollte die Allocate-Methode für die Firewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="12aeb-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="12aeb-115">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen der Firewall zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="12aeb-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="12aeb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="12aeb-116">PARAMETERS</span></span>

### <span data-ttu-id="12aeb-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12aeb-117">-AsJob</span></span>
<span data-ttu-id="12aeb-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="12aeb-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12aeb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12aeb-119">-DefaultProfile</span></span>
<span data-ttu-id="12aeb-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12aeb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12aeb-121">-Force</span><span class="sxs-lookup"><span data-stu-id="12aeb-121">-Force</span></span>
<span data-ttu-id="12aeb-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="12aeb-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12aeb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="12aeb-123">-Name</span></span>
<span data-ttu-id="12aeb-124">Gibt den Namen der Firewall an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="12aeb-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12aeb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12aeb-125">-PassThru</span></span>
<span data-ttu-id="12aeb-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="12aeb-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12aeb-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="12aeb-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12aeb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12aeb-128">-ResourceGroupName</span></span>
<span data-ttu-id="12aeb-129">Gibt den Namen der Ressourcengruppe an, die die vom Cmdlet entfernte Firewall enthält.</span><span class="sxs-lookup"><span data-stu-id="12aeb-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12aeb-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12aeb-130">-Confirm</span></span>
<span data-ttu-id="12aeb-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12aeb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12aeb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12aeb-132">-WhatIf</span></span>
<span data-ttu-id="12aeb-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12aeb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12aeb-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12aeb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12aeb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12aeb-135">CommonParameters</span></span>
<span data-ttu-id="12aeb-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12aeb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12aeb-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12aeb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12aeb-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12aeb-138">INPUTS</span></span>

### <span data-ttu-id="12aeb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="12aeb-139">System.String</span></span>

## <span data-ttu-id="12aeb-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12aeb-140">OUTPUTS</span></span>

### <span data-ttu-id="12aeb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12aeb-141">System.Boolean</span></span>

## <span data-ttu-id="12aeb-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="12aeb-142">NOTES</span></span>

## <span data-ttu-id="12aeb-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12aeb-143">RELATED LINKS</span></span>

[<span data-ttu-id="12aeb-144">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="12aeb-144">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="12aeb-145">Neu – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="12aeb-145">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="12aeb-146">Satz-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="12aeb-146">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
