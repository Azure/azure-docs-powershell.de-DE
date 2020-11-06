---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationCertificate.md
ms.openlocfilehash: d1230030f95d22d972aa537208b30f350ec9dbe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499242"
---
# <span data-ttu-id="9c34e-101">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="9c34e-101">Remove-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="9c34e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c34e-102">SYNOPSIS</span></span>
<span data-ttu-id="9c34e-103">Entfernt ein Automatisierungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="9c34e-103">Removes an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c34e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c34e-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c34e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c34e-105">DESCRIPTION</span></span>
<span data-ttu-id="9c34e-106">Das Cmdlet **Remove-AzureRmAutomationCertificate** entfernt ein Zertifikat aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9c34e-106">The **Remove-AzureRmAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="9c34e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c34e-107">EXAMPLES</span></span>

### <span data-ttu-id="9c34e-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="9c34e-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9c34e-109">Dieser Befehl entfernt ein Zertifikat mit dem Namen Cert01 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9c34e-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9c34e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c34e-110">PARAMETERS</span></span>

### <span data-ttu-id="9c34e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9c34e-111">-AutomationAccountName</span></span>
<span data-ttu-id="9c34e-112">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="9c34e-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="9c34e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9c34e-113">-Name</span></span>
<span data-ttu-id="9c34e-114">Gibt den Namen des Zertifikats an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9c34e-114">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c34e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c34e-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c34e-116">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="9c34e-116">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="9c34e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c34e-117">-Confirm</span></span>
<span data-ttu-id="9c34e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c34e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c34e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c34e-119">-WhatIf</span></span>
<span data-ttu-id="9c34e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c34e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c34e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c34e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c34e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c34e-122">-DefaultProfile</span></span>
<span data-ttu-id="9c34e-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9c34e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c34e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c34e-124">CommonParameters</span></span>
<span data-ttu-id="9c34e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c34e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c34e-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c34e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c34e-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c34e-127">INPUTS</span></span>

## <span data-ttu-id="9c34e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c34e-128">OUTPUTS</span></span>

## <span data-ttu-id="9c34e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c34e-129">NOTES</span></span>

## <span data-ttu-id="9c34e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c34e-130">RELATED LINKS</span></span>

[<span data-ttu-id="9c34e-131">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="9c34e-131">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="9c34e-132">Neu – AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="9c34e-132">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="9c34e-133">Satz-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="9c34e-133">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


