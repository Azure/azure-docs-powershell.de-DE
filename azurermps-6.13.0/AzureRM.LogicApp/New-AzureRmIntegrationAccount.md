---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: 7183078623c3be1826c98712fa41524643a4a68c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497418"
---
# <span data-ttu-id="ed4d2-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed4d2-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="ed4d2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed4d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4d2-103">Erstellt ein Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed4d2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed4d2-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed4d2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed4d2-105">DESCRIPTION</span></span>
<span data-ttu-id="ed4d2-106">Mit dem Cmdlet **New-AzureRmIntegrationAccount** wird ein Integrations Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="ed4d2-107">Dieses Cmdlet gibt ein Objekt zurück, das das Integrations Konto darstellt. Geben Sie einen Namen, einen Speicherort, einen Ressourcengruppennamen und einen SKU-Namen an.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="ed4d2-108">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="ed4d2-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ed4d2-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ed4d2-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ed4d2-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ed4d2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed4d2-113">EXAMPLES</span></span>

### <span data-ttu-id="ed4d2-114">Beispiel 1: Erstellen eines Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="ed4d2-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="ed4d2-115">Mit diesem Befehl wird ein Integrations Konto mit dem Namen IntegrationAccount31 in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="ed4d2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed4d2-116">PARAMETERS</span></span>

### <span data-ttu-id="ed4d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4d2-117">-DefaultProfile</span></span>
<span data-ttu-id="ed4d2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ed4d2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed4d2-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="ed4d2-119">-Location</span></span>
<span data-ttu-id="ed4d2-120">Gibt einen Speicherort für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="ed4d2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ed4d2-121">-Name</span></span>
<span data-ttu-id="ed4d2-122">Gibt einen Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="ed4d2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed4d2-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed4d2-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ed4d2-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="ed4d2-125">-Sku</span></span>
<span data-ttu-id="ed4d2-126">Gibt einen SKU-Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="ed4d2-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed4d2-127">-Confirm</span></span>
<span data-ttu-id="ed4d2-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed4d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed4d2-129">-WhatIf</span></span>
<span data-ttu-id="ed4d2-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed4d2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed4d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4d2-132">CommonParameters</span></span>
<span data-ttu-id="ed4d2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed4d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4d2-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed4d2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4d2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed4d2-135">INPUTS</span></span>

### <span data-ttu-id="ed4d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ed4d2-136">System.String</span></span>

## <span data-ttu-id="ed4d2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed4d2-137">OUTPUTS</span></span>

### <span data-ttu-id="ed4d2-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed4d2-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="ed4d2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed4d2-139">NOTES</span></span>

## <span data-ttu-id="ed4d2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed4d2-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed4d2-141">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed4d2-141">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="ed4d2-142">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed4d2-142">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="ed4d2-143">Satz-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed4d2-143">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


