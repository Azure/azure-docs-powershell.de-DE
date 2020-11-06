---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: 7498310c232fd623b131bdf9ae59136d9a4c500a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498478"
---
# <span data-ttu-id="1f50f-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1f50f-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="1f50f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f50f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f50f-103">Entfernt ein Automatisierungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="1f50f-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f50f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f50f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f50f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f50f-105">DESCRIPTION</span></span>
<span data-ttu-id="1f50f-106">Das Cmdlet **Remove-AzureRmAutomationCertificate** entfernt ein Zertifikat aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1f50f-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="1f50f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f50f-107">EXAMPLES</span></span>

### <span data-ttu-id="1f50f-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="1f50f-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1f50f-109">Dieser Befehl entfernt ein Zertifikat mit dem Namen Cert01 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1f50f-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1f50f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f50f-110">PARAMETERS</span></span>

### <span data-ttu-id="1f50f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f50f-111">-AutomationAccountName</span></span>
<span data-ttu-id="1f50f-112">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="1f50f-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="1f50f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f50f-113">-DefaultProfile</span></span>
<span data-ttu-id="1f50f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1f50f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f50f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1f50f-115">-Name</span></span>
<span data-ttu-id="1f50f-116">Gibt den Namen des Zertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1f50f-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1f50f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f50f-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f50f-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="1f50f-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="1f50f-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1f50f-119">-Confirm</span></span>
<span data-ttu-id="1f50f-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1f50f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f50f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f50f-121">-WhatIf</span></span>
<span data-ttu-id="1f50f-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f50f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f50f-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f50f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f50f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f50f-124">CommonParameters</span></span>
<span data-ttu-id="1f50f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f50f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f50f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f50f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f50f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f50f-127">INPUTS</span></span>

### <span data-ttu-id="1f50f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1f50f-128">System.String</span></span>

## <span data-ttu-id="1f50f-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f50f-129">OUTPUTS</span></span>

### <span data-ttu-id="1f50f-130">System. void</span><span class="sxs-lookup"><span data-stu-id="1f50f-130">System.Void</span></span>

## <span data-ttu-id="1f50f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f50f-131">NOTES</span></span>

## <span data-ttu-id="1f50f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f50f-132">RELATED LINKS</span></span>

[<span data-ttu-id="1f50f-133">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1f50f-133">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1f50f-134">Neu – AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1f50f-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1f50f-135">Satz-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1f50f-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


