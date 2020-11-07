---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: fc4696a26c10ace497c6ff64a7ac4c1ac49279c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657917"
---
# <span data-ttu-id="a0373-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a0373-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="a0373-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0373-102">SYNOPSIS</span></span>
<span data-ttu-id="a0373-103">Entfernt einen DSC-Knoten aus der Verwaltung durch ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="a0373-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="a0373-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0373-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0373-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0373-105">DESCRIPTION</span></span>
<span data-ttu-id="a0373-106">Das Cmdlet " **Unregister-AzAutomationDscNode** " entfernt einen APS-Knoten (Desired State Configuration, DSC) aus der Verwaltung durch ein Azure-Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="a0373-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="a0373-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0373-107">EXAMPLES</span></span>

### <span data-ttu-id="a0373-108">Beispiel 1: Entfernen eines Azure DSC-Knotens aus der Verwaltung durch ein Automatisierungs Konto</span><span class="sxs-lookup"><span data-stu-id="a0373-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="a0373-109">Mit diesem Befehl wird der DSC-Knoten, der die angegebene GUID hat, von der Verwaltung durch das Automatisierungs Konto mit dem Namen Contoso17 entfernt.</span><span class="sxs-lookup"><span data-stu-id="a0373-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a0373-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0373-110">PARAMETERS</span></span>

### <span data-ttu-id="a0373-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0373-111">-AutomationAccountName</span></span>
<span data-ttu-id="a0373-112">Gibt den Namen des Automatisierungs Kontos an, aus dem dieses Cmdlet einen DSC-Knoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="a0373-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="a0373-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0373-113">-DefaultProfile</span></span>
<span data-ttu-id="a0373-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0373-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0373-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a0373-115">-Force</span></span>
<span data-ttu-id="a0373-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a0373-116">ps_force</span></span>

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

### <span data-ttu-id="a0373-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a0373-117">-Id</span></span>
<span data-ttu-id="a0373-118">Gibt die eindeutige ID des DSC-Knotens an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="a0373-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0373-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0373-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0373-120">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet die Registrierung eines DSC-Knotens aufhebt.</span><span class="sxs-lookup"><span data-stu-id="a0373-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="a0373-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0373-121">-Confirm</span></span>
<span data-ttu-id="a0373-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0373-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0373-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0373-123">-WhatIf</span></span>
<span data-ttu-id="a0373-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0373-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0373-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0373-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0373-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0373-126">CommonParameters</span></span>
<span data-ttu-id="a0373-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0373-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0373-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0373-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0373-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0373-129">INPUTS</span></span>

### <span data-ttu-id="a0373-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a0373-130">System.Guid</span></span>

### <span data-ttu-id="a0373-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a0373-131">System.String</span></span>

## <span data-ttu-id="a0373-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0373-132">OUTPUTS</span></span>

### <span data-ttu-id="a0373-133">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="a0373-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="a0373-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0373-134">NOTES</span></span>

## <span data-ttu-id="a0373-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0373-135">RELATED LINKS</span></span>

[<span data-ttu-id="a0373-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a0373-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="a0373-137">Registrieren-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a0373-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="a0373-138">Satz-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a0373-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


