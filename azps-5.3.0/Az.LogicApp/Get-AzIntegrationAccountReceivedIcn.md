---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472315"
---
# <span data-ttu-id="dc4fa-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="dc4fa-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="dc4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="dc4fa-103">Dieses Cmdlet ruft eine bestimmte empfangene Austauschsteuerelementnummer pro Vertrag und Steuerelementnummerwert ab.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="dc4fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc4fa-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc4fa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc4fa-105">DESCRIPTION</span></span>
<span data-ttu-id="dc4fa-106">Dieses Cmdlet soll in Notfallwiederherstellungsszenarien verwendet werden, um das Vorhandensein der Nummer eines empfangenen Austauschsteuerelements zu überprüfen und optional diese Entität mit "Remove-AzIntegrationAccountReceivedIcn" zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="dc4fa-107">Geben Sie den Parameter "-AgreementType" an, um anzugeben, ob X12- oder Edifact-Steuerelementnummern zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="dc4fa-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dc4fa-108">EXAMPLES</span></span>

### <span data-ttu-id="dc4fa-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dc4fa-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="dc4fa-110">Mit diesem Befehl wird das X12-Integrationskonto, das die Nummer des Austauschsteuerelements erhält, nach Vertragsname und Steuerelementnummerwert ruft.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="dc4fa-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dc4fa-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="dc4fa-112">Mit diesem Befehl wird das Konto für die Edifact-Integration, bei dem die Austauschsteuerungsnummer nach Vertragsname und Steuerelementnummerwert empfangen wurde, empfangen.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="dc4fa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc4fa-113">PARAMETERS</span></span>

### <span data-ttu-id="dc4fa-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="dc4fa-114">-AgreementName</span></span>
<span data-ttu-id="dc4fa-115">Der Name des Vertrags für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="dc4fa-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="dc4fa-116">-AgreementType</span></span>
<span data-ttu-id="dc4fa-117">Der Typ des Vertrags für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="dc4fa-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="dc4fa-118">-ControlNumberValue</span></span>
<span data-ttu-id="dc4fa-119">Der Wert für die Nummer des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="dc4fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc4fa-120">-DefaultProfile</span></span>
<span data-ttu-id="dc4fa-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dc4fa-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc4fa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dc4fa-122">-Name</span></span>
<span data-ttu-id="dc4fa-123">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-123">The integration account name.</span></span>

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

### <span data-ttu-id="dc4fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc4fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc4fa-125">Der Name der Integrationskontoressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="dc4fa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc4fa-126">CommonParameters</span></span>
<span data-ttu-id="dc4fa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc4fa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc4fa-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc4fa-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc4fa-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dc4fa-129">INPUTS</span></span>

### <span data-ttu-id="dc4fa-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dc4fa-130">System.String</span></span>

## <span data-ttu-id="dc4fa-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dc4fa-131">OUTPUTS</span></span>

### <span data-ttu-id="dc4fa-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="dc4fa-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="dc4fa-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dc4fa-133">NOTES</span></span>

## <span data-ttu-id="dc4fa-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dc4fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="dc4fa-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="dc4fa-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="dc4fa-136">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="dc4fa-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
