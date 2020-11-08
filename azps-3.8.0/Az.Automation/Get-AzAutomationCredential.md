---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997415"
---
# <span data-ttu-id="20c72-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="20c72-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="20c72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20c72-102">SYNOPSIS</span></span>
<span data-ttu-id="20c72-103">Ruft Automatisierungs Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="20c72-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="20c72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20c72-104">SYNTAX</span></span>

### <span data-ttu-id="20c72-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="20c72-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c72-106">ByName</span><span class="sxs-lookup"><span data-stu-id="20c72-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c72-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20c72-107">DESCRIPTION</span></span>
<span data-ttu-id="20c72-108">Das Cmdlet " **Get-AzAutomationCredential** " ruft mindestens eine Azure-Automatisierungs Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="20c72-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="20c72-109">Standardmäßig werden alle Anmeldeinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="20c72-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="20c72-110">Geben Sie den Namen der Anmeldeinformationen an, um bestimmte Anmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="20c72-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="20c72-111">Aus Sicherheitsgründen gibt dieses Cmdlet keine Kennwörter für Anmeldeinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="20c72-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="20c72-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20c72-112">EXAMPLES</span></span>

### <span data-ttu-id="20c72-113">Beispiel 1: Abrufen aller Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="20c72-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="20c72-114">Dieser Befehl ruft Metadaten für alle Anmeldeinformationen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="20c72-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="20c72-115">Beispiel 2: Abrufen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="20c72-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="20c72-116">Dieser Befehl ruft Metadaten für die Anmeldeinformationen mit dem Namen ContosoCredential im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="20c72-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="20c72-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="20c72-117">PARAMETERS</span></span>

### <span data-ttu-id="20c72-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20c72-118">-AutomationAccountName</span></span>
<span data-ttu-id="20c72-119">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="20c72-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="20c72-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c72-120">-DefaultProfile</span></span>
<span data-ttu-id="20c72-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="20c72-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20c72-122">-Name</span><span class="sxs-lookup"><span data-stu-id="20c72-122">-Name</span></span>
<span data-ttu-id="20c72-123">Gibt den Namen der abzurufenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="20c72-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="20c72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20c72-124">-ResourceGroupName</span></span>
<span data-ttu-id="20c72-125">Gibt die Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="20c72-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="20c72-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c72-126">CommonParameters</span></span>
<span data-ttu-id="20c72-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c72-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c72-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20c72-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c72-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20c72-129">INPUTS</span></span>

### <span data-ttu-id="20c72-130">System. String</span><span class="sxs-lookup"><span data-stu-id="20c72-130">System.String</span></span>

## <span data-ttu-id="20c72-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20c72-131">OUTPUTS</span></span>

### <span data-ttu-id="20c72-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="20c72-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="20c72-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="20c72-133">NOTES</span></span>

## <span data-ttu-id="20c72-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20c72-134">RELATED LINKS</span></span>

[<span data-ttu-id="20c72-135">Neu – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="20c72-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="20c72-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="20c72-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="20c72-137">Satz-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="20c72-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


