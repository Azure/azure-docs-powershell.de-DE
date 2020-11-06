---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: b9defadc92619d136c82302203d296d6b71318ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482397"
---
# <span data-ttu-id="fb8be-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="fb8be-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="fb8be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb8be-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8be-103">Mit diesem Cmdlet wird eine bestimmte empfangene Austauschkontrollnummer pro Vereinbarung und Steuernummern Wert abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fb8be-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb8be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb8be-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb8be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb8be-105">DESCRIPTION</span></span>
<span data-ttu-id="fb8be-106">Dieses Cmdlet ist für die Verwendung in Disaster Recovery-Szenarien vorgesehen, um das vorhanden sein einer empfangenen Interchange-Kontrollnummer zu überprüfen und diese Entität optional mit Remove-AzureRmIntegrationAccountReceivedIcn zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fb8be-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="fb8be-107">Geben Sie den Parameter "-agreementtype" an, um anzugeben, ob X12-oder EDIFACT-Steuernummern zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fb8be-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="fb8be-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb8be-108">EXAMPLES</span></span>

### <span data-ttu-id="fb8be-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fb8be-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="fb8be-110">Dieser Befehl ruft das X12-Integrations Konto, das die Nummer des Austausch Kontrollgeräts erhält, nach Vertragsname und Steuernummern Wert ab.</span><span class="sxs-lookup"><span data-stu-id="fb8be-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="fb8be-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fb8be-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="fb8be-112">Dieser Befehl ruft das EDIFACT-Integrations Konto ab, das die Nummer des Austausch Steuerelements nach Vertragsname und Steuerelement-Nummernwert erhält.</span><span class="sxs-lookup"><span data-stu-id="fb8be-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="fb8be-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb8be-113">PARAMETERS</span></span>

### <span data-ttu-id="fb8be-114">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="fb8be-114">-AgreementName</span></span>
<span data-ttu-id="fb8be-115">Der Name des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="fb8be-115">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8be-116">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="fb8be-116">-AgreementType</span></span>
<span data-ttu-id="fb8be-117">Der Typ des Integrations kontovertrags.</span><span class="sxs-lookup"><span data-stu-id="fb8be-117">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8be-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="fb8be-118">-ControlNumberValue</span></span>
<span data-ttu-id="fb8be-119">Der Wert des Integrations Konto-Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="fb8be-119">The integration account control number value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8be-120">-DefaultProfile</span></span>
<span data-ttu-id="fb8be-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fb8be-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb8be-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fb8be-122">-Name</span></span>
<span data-ttu-id="fb8be-123">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="fb8be-123">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb8be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8be-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb8be-125">Der Name der Ressourcengruppe der Integrations Konten.</span><span class="sxs-lookup"><span data-stu-id="fb8be-125">The integration account resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8be-126">CommonParameters</span></span>
<span data-ttu-id="fb8be-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb8be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8be-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8be-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb8be-129">INPUTS</span></span>

### <span data-ttu-id="fb8be-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fb8be-130">System.String</span></span>

## <span data-ttu-id="fb8be-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb8be-131">OUTPUTS</span></span>

### <span data-ttu-id="fb8be-132">Microsoft. Azure. Commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="fb8be-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="fb8be-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb8be-133">NOTES</span></span>

## <span data-ttu-id="fb8be-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb8be-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb8be-135">Satz-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="fb8be-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="fb8be-136">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="fb8be-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
