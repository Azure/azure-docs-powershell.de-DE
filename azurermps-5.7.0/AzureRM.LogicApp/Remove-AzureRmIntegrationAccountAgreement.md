---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 88661e132e6f40f4bb8e90fac339ddf1946085c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663058"
---
# <span data-ttu-id="d9018-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d9018-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="d9018-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9018-102">SYNOPSIS</span></span>
<span data-ttu-id="d9018-103">Entfernt eine Integration-Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="d9018-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9018-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9018-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9018-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9018-105">DESCRIPTION</span></span>
<span data-ttu-id="d9018-106">Das Cmdlet **Remove-AzureRmIntegrationAccountAgreement** entfernt eine Integration-Kontovereinbarung aus einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9018-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="d9018-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="d9018-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="d9018-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="d9018-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d9018-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="d9018-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d9018-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d9018-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d9018-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="d9018-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d9018-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9018-112">EXAMPLES</span></span>

### <span data-ttu-id="d9018-113">Beispiel 1: Entfernen einer Integration-Kontovereinbarung nach Namen</span><span class="sxs-lookup"><span data-stu-id="d9018-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="d9018-114">Mit diesem Befehl wird der Integrations Kontovertrag mit dem Namen IntegrationAccountAgreement06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9018-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="d9018-115">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="d9018-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d9018-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9018-116">PARAMETERS</span></span>

### <span data-ttu-id="d9018-117">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="d9018-117">-AgreementName</span></span>
<span data-ttu-id="d9018-118">Gibt den Namen der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="d9018-118">Specifies the name of the integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9018-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9018-119">-DefaultProfile</span></span>
<span data-ttu-id="d9018-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d9018-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9018-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d9018-121">-Force</span></span>
<span data-ttu-id="d9018-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d9018-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9018-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d9018-123">-Name</span></span>
<span data-ttu-id="d9018-124">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d9018-124">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9018-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9018-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9018-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d9018-126">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9018-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9018-127">-Confirm</span></span>
<span data-ttu-id="d9018-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9018-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9018-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9018-129">-WhatIf</span></span>
<span data-ttu-id="d9018-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9018-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9018-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9018-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9018-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9018-132">CommonParameters</span></span>
<span data-ttu-id="d9018-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9018-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9018-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9018-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9018-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9018-135">INPUTS</span></span>

### <span data-ttu-id="d9018-136">Keine</span><span class="sxs-lookup"><span data-stu-id="d9018-136">None</span></span>
<span data-ttu-id="d9018-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d9018-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d9018-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9018-138">OUTPUTS</span></span>

## <span data-ttu-id="d9018-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9018-139">NOTES</span></span>

## <span data-ttu-id="d9018-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9018-140">RELATED LINKS</span></span>

[<span data-ttu-id="d9018-141">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d9018-141">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="d9018-142">Neu – AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d9018-142">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="d9018-143">Satz-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d9018-143">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


