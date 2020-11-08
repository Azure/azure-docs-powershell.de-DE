---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180357"
---
# <span data-ttu-id="12661-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="12661-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="12661-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12661-102">SYNOPSIS</span></span>
<span data-ttu-id="12661-103">Erstellt ein Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="12661-103">Creates an integration account.</span></span>

## <span data-ttu-id="12661-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12661-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12661-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12661-105">DESCRIPTION</span></span>
<span data-ttu-id="12661-106">Mit dem Cmdlet **New-AzIntegrationAccount** wird ein Integrations Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="12661-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="12661-107">Dieses Cmdlet gibt ein Objekt zurück, das das Integrations Konto darstellt. Geben Sie einen Namen, einen Speicherort, einen Ressourcengruppennamen und einen SKU-Namen an.</span><span class="sxs-lookup"><span data-stu-id="12661-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="12661-108">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="12661-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="12661-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="12661-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="12661-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="12661-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="12661-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="12661-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="12661-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="12661-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="12661-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12661-113">EXAMPLES</span></span>

### <span data-ttu-id="12661-114">Beispiel 1: Erstellen eines Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="12661-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="12661-115">Mit diesem Befehl wird ein Integrations Konto mit dem Namen IntegrationAccount31 in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="12661-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="12661-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="12661-116">PARAMETERS</span></span>

### <span data-ttu-id="12661-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12661-117">-DefaultProfile</span></span>
<span data-ttu-id="12661-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="12661-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12661-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="12661-119">-Location</span></span>
<span data-ttu-id="12661-120">Gibt einen Speicherort für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="12661-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="12661-121">-Name</span><span class="sxs-lookup"><span data-stu-id="12661-121">-Name</span></span>
<span data-ttu-id="12661-122">Gibt einen Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="12661-122">Specifies a name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12661-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12661-123">-ResourceGroupName</span></span>
<span data-ttu-id="12661-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="12661-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="12661-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="12661-125">-Sku</span></span>
<span data-ttu-id="12661-126">Gibt einen SKU-Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="12661-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12661-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12661-127">-Confirm</span></span>
<span data-ttu-id="12661-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12661-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12661-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12661-129">-WhatIf</span></span>
<span data-ttu-id="12661-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12661-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12661-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12661-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12661-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12661-132">CommonParameters</span></span>
<span data-ttu-id="12661-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12661-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12661-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12661-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12661-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12661-135">INPUTS</span></span>

### <span data-ttu-id="12661-136">System. String</span><span class="sxs-lookup"><span data-stu-id="12661-136">System.String</span></span>

## <span data-ttu-id="12661-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12661-137">OUTPUTS</span></span>

### <span data-ttu-id="12661-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="12661-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="12661-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="12661-139">NOTES</span></span>

## <span data-ttu-id="12661-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12661-140">RELATED LINKS</span></span>

[<span data-ttu-id="12661-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="12661-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="12661-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="12661-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="12661-143">Satz-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="12661-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


