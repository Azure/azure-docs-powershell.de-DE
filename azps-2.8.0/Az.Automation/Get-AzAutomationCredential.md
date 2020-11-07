---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3a13605618c5cda3c247cd6b0812732ce018bafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658071"
---
# <span data-ttu-id="5ae2c-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5ae2c-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="5ae2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ae2c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae2c-103">Ruft Automatisierungs Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="5ae2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ae2c-104">SYNTAX</span></span>

### <span data-ttu-id="5ae2c-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ae2c-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ae2c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5ae2c-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ae2c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ae2c-107">DESCRIPTION</span></span>
<span data-ttu-id="5ae2c-108">Das Cmdlet " **Get-AzAutomationCredential** " ruft mindestens eine Azure-Automatisierungs Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="5ae2c-109">Standardmäßig werden alle Anmeldeinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="5ae2c-110">Geben Sie den Namen der Anmeldeinformationen an, um bestimmte Anmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="5ae2c-111">Aus Sicherheitsgründen gibt dieses Cmdlet keine Kennwörter für Anmeldeinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="5ae2c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ae2c-112">EXAMPLES</span></span>

### <span data-ttu-id="5ae2c-113">Beispiel 1: Abrufen aller Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5ae2c-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5ae2c-114">Dieser Befehl ruft Metadaten für alle Anmeldeinformationen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5ae2c-115">Beispiel 2: Abrufen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5ae2c-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="5ae2c-116">Dieser Befehl ruft Metadaten für die Anmeldeinformationen mit dem Namen ContosoCredential im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5ae2c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ae2c-117">PARAMETERS</span></span>

### <span data-ttu-id="5ae2c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5ae2c-118">-AutomationAccountName</span></span>
<span data-ttu-id="5ae2c-119">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="5ae2c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ae2c-120">-DefaultProfile</span></span>
<span data-ttu-id="5ae2c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5ae2c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ae2c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5ae2c-122">-Name</span></span>
<span data-ttu-id="5ae2c-123">Gibt den Namen der abzurufenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="5ae2c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ae2c-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ae2c-125">Gibt die Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="5ae2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae2c-126">CommonParameters</span></span>
<span data-ttu-id="5ae2c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae2c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ae2c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae2c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ae2c-129">INPUTS</span></span>

### <span data-ttu-id="5ae2c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5ae2c-130">System.String</span></span>

## <span data-ttu-id="5ae2c-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ae2c-131">OUTPUTS</span></span>

### <span data-ttu-id="5ae2c-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="5ae2c-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="5ae2c-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ae2c-133">NOTES</span></span>

## <span data-ttu-id="5ae2c-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ae2c-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ae2c-135">Neu – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5ae2c-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="5ae2c-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5ae2c-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="5ae2c-137">Satz-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5ae2c-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


