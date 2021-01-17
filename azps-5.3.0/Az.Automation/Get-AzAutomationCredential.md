---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471379"
---
# <span data-ttu-id="70e37-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="70e37-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="70e37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70e37-102">SYNOPSIS</span></span>
<span data-ttu-id="70e37-103">Ruft Automatisierungsanmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="70e37-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="70e37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70e37-104">SYNTAX</span></span>

### <span data-ttu-id="70e37-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="70e37-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70e37-106">ByName</span><span class="sxs-lookup"><span data-stu-id="70e37-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70e37-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70e37-107">DESCRIPTION</span></span>
<span data-ttu-id="70e37-108">Das **Cmdlet "Get-AzAutomationCredential"** ruft mindestens eine Azure -Automatisierungsanmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="70e37-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="70e37-109">Standardmäßig werden alle Anmeldeinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="70e37-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="70e37-110">Geben Sie den Namen einer Anmeldeinformationen an, um bestimmte Anmeldeinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="70e37-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="70e37-111">Aus Sicherheitsgründen gibt dieses Cmdlet keine Anmeldeinformationskennwörter zurück.</span><span class="sxs-lookup"><span data-stu-id="70e37-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="70e37-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="70e37-112">EXAMPLES</span></span>

### <span data-ttu-id="70e37-113">Beispiel 1: Alle Anmeldeinformationen erhalten</span><span class="sxs-lookup"><span data-stu-id="70e37-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="70e37-114">Dieser Befehl ruft Metadaten für alle Anmeldeinformationen im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="70e37-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="70e37-115">Beispiel 2: Erhalten von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="70e37-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="70e37-116">Dieser Befehl ruft Metadaten für die Anmeldeinformationen namens "ContosoCredential" im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="70e37-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="70e37-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70e37-117">PARAMETERS</span></span>

### <span data-ttu-id="70e37-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70e37-118">-AutomationAccountName</span></span>
<span data-ttu-id="70e37-119">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="70e37-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="70e37-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e37-120">-DefaultProfile</span></span>
<span data-ttu-id="70e37-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="70e37-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70e37-122">-Name</span><span class="sxs-lookup"><span data-stu-id="70e37-122">-Name</span></span>
<span data-ttu-id="70e37-123">Gibt den Namen der abzurufenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="70e37-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="70e37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e37-124">-ResourceGroupName</span></span>
<span data-ttu-id="70e37-125">Gibt die Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="70e37-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="70e37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e37-126">CommonParameters</span></span>
<span data-ttu-id="70e37-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70e37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e37-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e37-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e37-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="70e37-129">INPUTS</span></span>

### <span data-ttu-id="70e37-130">System.String</span><span class="sxs-lookup"><span data-stu-id="70e37-130">System.String</span></span>

## <span data-ttu-id="70e37-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="70e37-131">OUTPUTS</span></span>

### <span data-ttu-id="70e37-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="70e37-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="70e37-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="70e37-133">NOTES</span></span>

## <span data-ttu-id="70e37-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="70e37-134">RELATED LINKS</span></span>

[<span data-ttu-id="70e37-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="70e37-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="70e37-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="70e37-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="70e37-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="70e37-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


