---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C0B24E18-9163-458A-8297-93CB5C2003FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCertificate.md
ms.openlocfilehash: e6dd090998d7a61d61fdad4bb40cbe2c62d7df1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171708"
---
# <span data-ttu-id="18f14-101">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="18f14-101">Remove-AzAutomationCertificate</span></span>

## <span data-ttu-id="18f14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18f14-102">SYNOPSIS</span></span>
<span data-ttu-id="18f14-103">Entfernt ein Automatisierungszertifikat.</span><span class="sxs-lookup"><span data-stu-id="18f14-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="18f14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18f14-104">SYNTAX</span></span>

```
Remove-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18f14-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18f14-105">DESCRIPTION</span></span>
<span data-ttu-id="18f14-106">Das **Cmdlet "Remove-AzAutomationCertificate"** entfernt ein Zertifikat aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="18f14-106">The **Remove-AzAutomationCertificate** cmdlet removes a certificate from Azure Automation.</span></span>

## <span data-ttu-id="18f14-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="18f14-107">EXAMPLES</span></span>

### <span data-ttu-id="18f14-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="18f14-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="18f14-109">Mit diesem Befehl wird ein Zertifikat namens "Cert01" im Automatisierungskonto namens "Contoso17" entfernt.</span><span class="sxs-lookup"><span data-stu-id="18f14-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="18f14-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18f14-110">PARAMETERS</span></span>

### <span data-ttu-id="18f14-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="18f14-111">-AutomationAccountName</span></span>
<span data-ttu-id="18f14-112">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="18f14-112">Specifies the name of the Automation account for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="18f14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18f14-113">-DefaultProfile</span></span>
<span data-ttu-id="18f14-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="18f14-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18f14-115">-Name</span><span class="sxs-lookup"><span data-stu-id="18f14-115">-Name</span></span>
<span data-ttu-id="18f14-116">Gibt den Namen des Zertifikats an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="18f14-116">Specifies the name of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="18f14-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18f14-117">-ResourceGroupName</span></span>
<span data-ttu-id="18f14-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="18f14-118">Specifies the name of the resource group for which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="18f14-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18f14-119">-Confirm</span></span>
<span data-ttu-id="18f14-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18f14-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18f14-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="18f14-121">-WhatIf</span></span>
<span data-ttu-id="18f14-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18f14-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18f14-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18f14-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18f14-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f14-124">CommonParameters</span></span>
<span data-ttu-id="18f14-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18f14-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f14-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f14-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f14-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="18f14-127">INPUTS</span></span>

### <span data-ttu-id="18f14-128">System.String</span><span class="sxs-lookup"><span data-stu-id="18f14-128">System.String</span></span>

## <span data-ttu-id="18f14-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="18f14-129">OUTPUTS</span></span>

### <span data-ttu-id="18f14-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="18f14-130">System.Void</span></span>

## <span data-ttu-id="18f14-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="18f14-131">NOTES</span></span>

## <span data-ttu-id="18f14-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="18f14-132">RELATED LINKS</span></span>

[<span data-ttu-id="18f14-133">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="18f14-133">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="18f14-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="18f14-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="18f14-135">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="18f14-135">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


