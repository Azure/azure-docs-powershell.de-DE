---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180339"
---
# <span data-ttu-id="cb83c-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cb83c-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="cb83c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cb83c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb83c-103">Entfernt eine Integration-Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="cb83c-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="cb83c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb83c-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb83c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb83c-105">DESCRIPTION</span></span>
<span data-ttu-id="cb83c-106">Das Cmdlet **Remove-AzIntegrationAccountAgreement** entfernt eine Integration-Kontovereinbarung aus einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cb83c-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="cb83c-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="cb83c-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="cb83c-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb83c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cb83c-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="cb83c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cb83c-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="cb83c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cb83c-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="cb83c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cb83c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cb83c-112">EXAMPLES</span></span>

### <span data-ttu-id="cb83c-113">Beispiel 1: Entfernen einer Integration-Kontovereinbarung nach Namen</span><span class="sxs-lookup"><span data-stu-id="cb83c-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="cb83c-114">Mit diesem Befehl wird der Integrations Kontovertrag mit dem Namen IntegrationAccountAgreement06 entfernt.</span><span class="sxs-lookup"><span data-stu-id="cb83c-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="cb83c-115">Der Befehl fordert Sie nicht zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="cb83c-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cb83c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb83c-116">PARAMETERS</span></span>

### <span data-ttu-id="cb83c-117">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="cb83c-117">-AgreementName</span></span>
<span data-ttu-id="cb83c-118">Gibt den Namen der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="cb83c-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="cb83c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb83c-119">-DefaultProfile</span></span>
<span data-ttu-id="cb83c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="cb83c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb83c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cb83c-121">-Force</span></span>
<span data-ttu-id="cb83c-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="cb83c-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb83c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cb83c-123">-Name</span></span>
<span data-ttu-id="cb83c-124">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="cb83c-124">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb83c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb83c-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb83c-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cb83c-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cb83c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cb83c-127">-Confirm</span></span>
<span data-ttu-id="cb83c-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb83c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb83c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb83c-129">-WhatIf</span></span>
<span data-ttu-id="cb83c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb83c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb83c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb83c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb83c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb83c-132">CommonParameters</span></span>
<span data-ttu-id="cb83c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb83c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb83c-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb83c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb83c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cb83c-135">INPUTS</span></span>

### <span data-ttu-id="cb83c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cb83c-136">System.String</span></span>

## <span data-ttu-id="cb83c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cb83c-137">OUTPUTS</span></span>

### <span data-ttu-id="cb83c-138">System. void</span><span class="sxs-lookup"><span data-stu-id="cb83c-138">System.Void</span></span>

## <span data-ttu-id="cb83c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="cb83c-139">NOTES</span></span>

## <span data-ttu-id="cb83c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cb83c-140">RELATED LINKS</span></span>

[<span data-ttu-id="cb83c-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cb83c-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cb83c-142">Neu – AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cb83c-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="cb83c-143">Satz-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cb83c-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


