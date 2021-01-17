---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469472"
---
# <span data-ttu-id="dfd84-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd84-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="dfd84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfd84-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd84-103">Entfernt ein Zertifikat für ein Integrationskonto aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dfd84-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="dfd84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfd84-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfd84-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfd84-105">DESCRIPTION</span></span>
<span data-ttu-id="dfd84-106">Das **Cmdlet "Remove-AzIntegrationAccountCertificate"** entfernt ein Integrationskontozertifikat aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dfd84-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="dfd84-107">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Zertifikatnamen an.</span><span class="sxs-lookup"><span data-stu-id="dfd84-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="dfd84-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="dfd84-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dfd84-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="dfd84-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dfd84-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="dfd84-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dfd84-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="dfd84-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dfd84-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dfd84-112">EXAMPLES</span></span>

### <span data-ttu-id="dfd84-113">Beispiel 1: Entfernen eines Zertifikats für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="dfd84-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="dfd84-114">Mit diesem Befehl wird das Zertifikat für das Integrationskonto namens "IntegrationAccount31" entfernt.</span><span class="sxs-lookup"><span data-stu-id="dfd84-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="dfd84-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfd84-115">PARAMETERS</span></span>

### <span data-ttu-id="dfd84-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="dfd84-116">-CertificateName</span></span>
<span data-ttu-id="dfd84-117">Gibt den Namen eines Zertifikats für ein Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="dfd84-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="dfd84-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd84-118">-DefaultProfile</span></span>
<span data-ttu-id="dfd84-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dfd84-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfd84-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dfd84-120">-Force</span></span>
<span data-ttu-id="dfd84-121">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="dfd84-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dfd84-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dfd84-122">-Name</span></span>
<span data-ttu-id="dfd84-123">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="dfd84-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="dfd84-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd84-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfd84-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dfd84-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dfd84-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfd84-126">-Confirm</span></span>
<span data-ttu-id="dfd84-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfd84-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfd84-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dfd84-128">-WhatIf</span></span>
<span data-ttu-id="dfd84-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfd84-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd84-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfd84-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfd84-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd84-131">CommonParameters</span></span>
<span data-ttu-id="dfd84-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd84-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd84-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd84-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd84-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dfd84-134">INPUTS</span></span>

### <span data-ttu-id="dfd84-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dfd84-135">System.String</span></span>

## <span data-ttu-id="dfd84-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dfd84-136">OUTPUTS</span></span>

### <span data-ttu-id="dfd84-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="dfd84-137">System.Void</span></span>

## <span data-ttu-id="dfd84-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dfd84-138">NOTES</span></span>

## <span data-ttu-id="dfd84-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dfd84-139">RELATED LINKS</span></span>

[<span data-ttu-id="dfd84-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd84-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="dfd84-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd84-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="dfd84-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dfd84-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


