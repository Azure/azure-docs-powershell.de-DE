---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: 9932627e94a27c1b29d20a5a6bc49d47a55d3ef5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657982"
---
# <span data-ttu-id="8b2e2-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8b2e2-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="8b2e2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2e2-103">Entfernt ein Automatisierungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="8b2e2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b2e2-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b2e2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b2e2-105">DESCRIPTION</span></span>
<span data-ttu-id="8b2e2-106">Das Cmdlet **Remove-AzAutomationCertificate** entfernt ein Zertifikat aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="8b2e2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b2e2-107">EXAMPLES</span></span>

### <span data-ttu-id="8b2e2-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="8b2e2-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8b2e2-109">Dieser Befehl entfernt ein Zertifikat mit dem Namen Cert01 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8b2e2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b2e2-110">PARAMETERS</span></span>

### <span data-ttu-id="8b2e2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8b2e2-111">-AutomationAccountName</span></span>
<span data-ttu-id="8b2e2-112">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="8b2e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2e2-113">-DefaultProfile</span></span>
<span data-ttu-id="8b2e2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8b2e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b2e2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b2e2-115">-Name</span></span>
<span data-ttu-id="8b2e2-116">Gibt den Namen des Zertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8b2e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b2e2-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="8b2e2-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b2e2-119">-Confirm</span></span>
<span data-ttu-id="8b2e2-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b2e2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b2e2-121">-WhatIf</span></span>
<span data-ttu-id="8b2e2-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b2e2-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b2e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2e2-124">CommonParameters</span></span>
<span data-ttu-id="8b2e2-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b2e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2e2-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b2e2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2e2-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b2e2-127">INPUTS</span></span>

### <span data-ttu-id="8b2e2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8b2e2-128">System.String</span></span>

## <span data-ttu-id="8b2e2-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b2e2-129">OUTPUTS</span></span>

### <span data-ttu-id="8b2e2-130">System. void</span><span class="sxs-lookup"><span data-stu-id="8b2e2-130">System.Void</span></span>

## <span data-ttu-id="8b2e2-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b2e2-131">NOTES</span></span>

## <span data-ttu-id="8b2e2-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b2e2-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b2e2-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8b2e2-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="8b2e2-134">Neu – AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8b2e2-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="8b2e2-135">Satz-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8b2e2-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


