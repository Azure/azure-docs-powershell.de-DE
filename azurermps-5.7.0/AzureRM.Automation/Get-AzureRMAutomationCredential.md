---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: 5f6ff2e89bd3b84a573e02a4584fe69794829453
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662384"
---
# <span data-ttu-id="94ddb-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94ddb-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="94ddb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="94ddb-103">Ruft Automatisierungs Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="94ddb-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94ddb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94ddb-104">SYNTAX</span></span>

### <span data-ttu-id="94ddb-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="94ddb-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94ddb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="94ddb-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94ddb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94ddb-107">DESCRIPTION</span></span>
<span data-ttu-id="94ddb-108">Das Cmdlet " **Get-AzureRmAutomationCredential** " ruft mindestens eine Azure-Automatisierungs Anmeldeinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="94ddb-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="94ddb-109">Standardmäßig werden alle Anmeldeinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="94ddb-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="94ddb-110">Geben Sie den Namen der Anmeldeinformationen an, um bestimmte Anmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="94ddb-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="94ddb-111">Aus Sicherheitsgründen gibt dieses Cmdlet keine Kennwörter für Anmeldeinformationen zurück.</span><span class="sxs-lookup"><span data-stu-id="94ddb-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="94ddb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94ddb-112">EXAMPLES</span></span>

### <span data-ttu-id="94ddb-113">Beispiel 1: Abrufen aller Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="94ddb-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="94ddb-114">Dieser Befehl ruft Metadaten für alle Anmeldeinformationen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="94ddb-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="94ddb-115">Beispiel 2: Abrufen von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="94ddb-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="94ddb-116">Dieser Befehl ruft Metadaten für die Anmeldeinformationen mit dem Namen ContosoCredential im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="94ddb-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="94ddb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="94ddb-117">PARAMETERS</span></span>

### <span data-ttu-id="94ddb-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94ddb-118">-AutomationAccountName</span></span>
<span data-ttu-id="94ddb-119">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="94ddb-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ddb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94ddb-120">-DefaultProfile</span></span>
<span data-ttu-id="94ddb-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="94ddb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94ddb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="94ddb-122">-Name</span></span>
<span data-ttu-id="94ddb-123">Gibt den Namen der abzurufenden Anmeldeinformationen an.</span><span class="sxs-lookup"><span data-stu-id="94ddb-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ddb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94ddb-124">-ResourceGroupName</span></span>
<span data-ttu-id="94ddb-125">Gibt die Ressourcengruppe an, für die dieses Cmdlet Anmeldeinformationen abruft.</span><span class="sxs-lookup"><span data-stu-id="94ddb-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94ddb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94ddb-126">CommonParameters</span></span>
<span data-ttu-id="94ddb-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94ddb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94ddb-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94ddb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94ddb-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94ddb-129">INPUTS</span></span>

### <span data-ttu-id="94ddb-130">Keine</span><span class="sxs-lookup"><span data-stu-id="94ddb-130">None</span></span>
<span data-ttu-id="94ddb-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="94ddb-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94ddb-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94ddb-132">OUTPUTS</span></span>

### <span data-ttu-id="94ddb-133">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="94ddb-133">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="94ddb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="94ddb-134">NOTES</span></span>

## <span data-ttu-id="94ddb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94ddb-135">RELATED LINKS</span></span>

[<span data-ttu-id="94ddb-136">Neu – AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94ddb-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="94ddb-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94ddb-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="94ddb-138">Satz-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94ddb-138">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


