---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: f10bd8d57cd70004ed37f16234aa72dd3a1a8ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939768"
---
# <span data-ttu-id="5280d-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5280d-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="5280d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5280d-102">SYNOPSIS</span></span>
<span data-ttu-id="5280d-103">Ruft Automatisierungsanmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="5280d-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="5280d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5280d-104">SYNTAX</span></span>

### <span data-ttu-id="5280d-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="5280d-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5280d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5280d-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5280d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5280d-107">DESCRIPTION</span></span>
<span data-ttu-id="5280d-108">Das **Get-AzAutomationCredential-Cmdlet** erhält mindestens eine Azure Automation-Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="5280d-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="5280d-109">Standardmäßig werden alle Anmeldeinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5280d-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="5280d-110">Geben Sie den Namen einer Anmeldeinformationen an, um eine bestimmte Anmeldeinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5280d-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="5280d-111">Aus Sicherheitsgründen gibt dieses Cmdlet keine Kennwörter für Anmeldeinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="5280d-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="5280d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5280d-112">EXAMPLES</span></span>

### <span data-ttu-id="5280d-113">Beispiel 1: Alle Anmeldeinformationen erhalten</span><span class="sxs-lookup"><span data-stu-id="5280d-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5280d-114">Dieser Befehl ruft Metadaten für alle Anmeldeinformationen im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="5280d-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5280d-115">Beispiel 2: Erhalten einer Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5280d-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="5280d-116">Dieser Befehl ruft Metadaten für die Anmeldeinformationen namens ContosoCredential im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="5280d-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5280d-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5280d-117">PARAMETERS</span></span>

### <span data-ttu-id="5280d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5280d-118">-AutomationAccountName</span></span>
<span data-ttu-id="5280d-119">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="5280d-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="5280d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5280d-120">-DefaultProfile</span></span>
<span data-ttu-id="5280d-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5280d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5280d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5280d-122">-Name</span></span>
<span data-ttu-id="5280d-123">Gibt den Namen einer abzurufenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="5280d-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5280d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5280d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5280d-125">Gibt die Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="5280d-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="5280d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5280d-126">CommonParameters</span></span>
<span data-ttu-id="5280d-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5280d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5280d-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5280d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5280d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5280d-129">INPUTS</span></span>

### <span data-ttu-id="5280d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5280d-130">System.String</span></span>

## <span data-ttu-id="5280d-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5280d-131">OUTPUTS</span></span>

### <span data-ttu-id="5280d-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="5280d-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="5280d-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5280d-133">NOTES</span></span>

## <span data-ttu-id="5280d-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5280d-134">RELATED LINKS</span></span>

[<span data-ttu-id="5280d-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5280d-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="5280d-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5280d-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="5280d-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5280d-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


