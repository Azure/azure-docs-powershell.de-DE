---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: c6f86d31f97ac0f4fcdbdd45c6bc111eda045800
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662810"
---
# <span data-ttu-id="28c80-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="28c80-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="28c80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28c80-102">SYNOPSIS</span></span>
<span data-ttu-id="28c80-103">Ändert ein Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="28c80-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28c80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28c80-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c80-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28c80-105">DESCRIPTION</span></span>
<span data-ttu-id="28c80-106">Das Cmdlet " **Satz-AzureRmIntegrationAccount** " ändert ein Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="28c80-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="28c80-107">Dieses Cmdlet gibt ein Objekt zurück, das das Integrations Konto darstellt.</span><span class="sxs-lookup"><span data-stu-id="28c80-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="28c80-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="28c80-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="28c80-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="28c80-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="28c80-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="28c80-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="28c80-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="28c80-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="28c80-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28c80-112">EXAMPLES</span></span>

### <span data-ttu-id="28c80-113">Beispiel 1: Ändern eines Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="28c80-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="28c80-114">Mit diesem Befehl wird ein Integrations Konto mit dem Namen IntegrationAccount31 in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="28c80-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="28c80-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="28c80-115">PARAMETERS</span></span>

### <span data-ttu-id="28c80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c80-116">-DefaultProfile</span></span>
<span data-ttu-id="28c80-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="28c80-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28c80-118">-Force</span><span class="sxs-lookup"><span data-stu-id="28c80-118">-Force</span></span>
<span data-ttu-id="28c80-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="28c80-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c80-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="28c80-120">-Location</span></span>
<span data-ttu-id="28c80-121">Gibt einen Speicherort für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="28c80-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="28c80-122">-Name</span><span class="sxs-lookup"><span data-stu-id="28c80-122">-Name</span></span>
<span data-ttu-id="28c80-123">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="28c80-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="28c80-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c80-124">-ResourceGroupName</span></span>
<span data-ttu-id="28c80-125">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="28c80-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="28c80-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="28c80-126">-Sku</span></span>
<span data-ttu-id="28c80-127">Gibt einen SKU-Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="28c80-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="28c80-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28c80-128">-Confirm</span></span>
<span data-ttu-id="28c80-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28c80-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28c80-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c80-130">-WhatIf</span></span>
<span data-ttu-id="28c80-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28c80-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c80-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28c80-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28c80-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c80-133">CommonParameters</span></span>
<span data-ttu-id="28c80-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c80-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c80-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28c80-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c80-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28c80-136">INPUTS</span></span>

### <span data-ttu-id="28c80-137">System. String</span><span class="sxs-lookup"><span data-stu-id="28c80-137">System.String</span></span>

## <span data-ttu-id="28c80-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28c80-138">OUTPUTS</span></span>

### <span data-ttu-id="28c80-139">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="28c80-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="28c80-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="28c80-140">NOTES</span></span>

## <span data-ttu-id="28c80-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28c80-141">RELATED LINKS</span></span>

[<span data-ttu-id="28c80-142">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="28c80-142">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="28c80-143">Neu – AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="28c80-143">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="28c80-144">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="28c80-144">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


