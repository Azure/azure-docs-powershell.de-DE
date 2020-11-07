---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846323"
---
# <span data-ttu-id="d9cb9-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d9cb9-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="d9cb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9cb9-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cb9-103">Entfernt einen DSC-Knoten aus der Verwaltung durch ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="d9cb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9cb9-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9cb9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9cb9-105">DESCRIPTION</span></span>
<span data-ttu-id="d9cb9-106">Das Cmdlet " **Unregister-AzAutomationDscNode** " entfernt einen APS-Knoten (Desired State Configuration, DSC) aus der Verwaltung durch ein Azure-Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="d9cb9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9cb9-107">EXAMPLES</span></span>

### <span data-ttu-id="d9cb9-108">Beispiel 1: Entfernen eines Azure DSC-Knotens aus der Verwaltung durch ein Automatisierungs Konto</span><span class="sxs-lookup"><span data-stu-id="d9cb9-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="d9cb9-109">Mit diesem Befehl wird der DSC-Knoten, der die angegebene GUID hat, von der Verwaltung durch das Automatisierungs Konto mit dem Namen Contoso17 entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d9cb9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9cb9-110">PARAMETERS</span></span>

### <span data-ttu-id="d9cb9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d9cb9-111">-AutomationAccountName</span></span>
<span data-ttu-id="d9cb9-112">Gibt den Namen des Automatisierungs Kontos an, aus dem dieses Cmdlet einen DSC-Knoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="d9cb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cb9-113">-DefaultProfile</span></span>
<span data-ttu-id="d9cb9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d9cb9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9cb9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d9cb9-115">-Force</span></span>
<span data-ttu-id="d9cb9-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="d9cb9-116">ps_force</span></span>

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

### <span data-ttu-id="d9cb9-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d9cb9-117">-Id</span></span>
<span data-ttu-id="d9cb9-118">Gibt die eindeutige ID des DSC-Knotens an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d9cb9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9cb9-119">-ResourceGroupName</span></span>
<span data-ttu-id="d9cb9-120">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet die Registrierung eines DSC-Knotens aufhebt.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="d9cb9-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9cb9-121">-Confirm</span></span>
<span data-ttu-id="d9cb9-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9cb9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9cb9-123">-WhatIf</span></span>
<span data-ttu-id="d9cb9-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9cb9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9cb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cb9-126">CommonParameters</span></span>
<span data-ttu-id="d9cb9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9cb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cb9-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9cb9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cb9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9cb9-129">INPUTS</span></span>

### <span data-ttu-id="d9cb9-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d9cb9-130">System.Guid</span></span>

### <span data-ttu-id="d9cb9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d9cb9-131">System.String</span></span>

## <span data-ttu-id="d9cb9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9cb9-132">OUTPUTS</span></span>

### <span data-ttu-id="d9cb9-133">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="d9cb9-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="d9cb9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9cb9-134">NOTES</span></span>

## <span data-ttu-id="d9cb9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9cb9-135">RELATED LINKS</span></span>

[<span data-ttu-id="d9cb9-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d9cb9-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="d9cb9-137">Registrieren-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d9cb9-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="d9cb9-138">Satz-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d9cb9-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


