---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: ad4954a8344fd34e881c9bae75d6ba31f9d099a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650778"
---
# <span data-ttu-id="abd6d-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="abd6d-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="abd6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abd6d-102">SYNOPSIS</span></span>
<span data-ttu-id="abd6d-103">Ruft eine Integration-Kontozuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="abd6d-103">Gets an integration account map.</span></span>

## <span data-ttu-id="abd6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abd6d-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abd6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abd6d-105">DESCRIPTION</span></span>
<span data-ttu-id="abd6d-106">Das Cmdlet " **Get-AzIntegrationAccountMap** " Ruft die Integration-Kontozuordnung aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="abd6d-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="abd6d-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Kartennamen an.</span><span class="sxs-lookup"><span data-stu-id="abd6d-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="abd6d-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="abd6d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="abd6d-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="abd6d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="abd6d-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="abd6d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="abd6d-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="abd6d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="abd6d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abd6d-112">EXAMPLES</span></span>

### <span data-ttu-id="abd6d-113">Beispiel 1: Abrufen einer Integrations Kontozuordnung</span><span class="sxs-lookup"><span data-stu-id="abd6d-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="abd6d-114">Dieser Befehl ruft eine Integration-Kontozuordnung mit dem Namen IntegrationAccountMap47 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="abd6d-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="abd6d-115">Beispiel 2: Abrufen von Integrations Kontozuordnungen nach dem Namen des Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="abd6d-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="abd6d-116">Mit diesem Befehl werden die Integrations Kontozuordnungen nach dem Namen des Integrations Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="abd6d-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="abd6d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="abd6d-117">PARAMETERS</span></span>

### <span data-ttu-id="abd6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd6d-118">-DefaultProfile</span></span>
<span data-ttu-id="abd6d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="abd6d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="abd6d-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="abd6d-120">-MapName</span></span>
<span data-ttu-id="abd6d-121">Gibt den Namen einer Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="abd6d-121">Specifies the name of an integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd6d-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="abd6d-122">-MapType</span></span>
<span data-ttu-id="abd6d-123">Der Zuordnungstyp des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="abd6d-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd6d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="abd6d-124">-Name</span></span>
<span data-ttu-id="abd6d-125">Gibt den Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="abd6d-125">Specifies the name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd6d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd6d-126">-ResourceGroupName</span></span>
<span data-ttu-id="abd6d-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="abd6d-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abd6d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd6d-128">CommonParameters</span></span>
<span data-ttu-id="abd6d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd6d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd6d-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd6d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd6d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abd6d-131">INPUTS</span></span>

### <span data-ttu-id="abd6d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="abd6d-132">System.String</span></span>

## <span data-ttu-id="abd6d-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abd6d-133">OUTPUTS</span></span>

### <span data-ttu-id="abd6d-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="abd6d-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="abd6d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="abd6d-135">NOTES</span></span>

## <span data-ttu-id="abd6d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abd6d-136">RELATED LINKS</span></span>

[<span data-ttu-id="abd6d-137">Neu – AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="abd6d-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="abd6d-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="abd6d-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="abd6d-139">Satz-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="abd6d-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


