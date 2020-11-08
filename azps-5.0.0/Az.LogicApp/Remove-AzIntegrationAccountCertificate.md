---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179171"
---
# <span data-ttu-id="f9734-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f9734-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="f9734-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9734-102">SYNOPSIS</span></span>
<span data-ttu-id="f9734-103">Entfernt ein Integrations Kontozertifikat aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9734-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="f9734-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9734-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9734-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9734-105">DESCRIPTION</span></span>
<span data-ttu-id="f9734-106">Das Cmdlet **Remove-AzIntegrationAccountCertificate** entfernt ein Integrations Kontozertifikat aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f9734-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="f9734-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="f9734-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="f9734-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9734-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f9734-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="f9734-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f9734-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="f9734-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f9734-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="f9734-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f9734-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9734-112">EXAMPLES</span></span>

### <span data-ttu-id="f9734-113">Beispiel 1: Entfernen eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="f9734-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="f9734-114">Mit diesem Befehl wird das Integrations Kontozertifikat mit dem Namen IntegrationAccount31 entfernt.</span><span class="sxs-lookup"><span data-stu-id="f9734-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="f9734-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9734-115">PARAMETERS</span></span>

### <span data-ttu-id="f9734-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="f9734-116">-CertificateName</span></span>
<span data-ttu-id="f9734-117">Gibt den Namen eines Integrations Kontozertifikats an.</span><span class="sxs-lookup"><span data-stu-id="f9734-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="f9734-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9734-118">-DefaultProfile</span></span>
<span data-ttu-id="f9734-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f9734-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9734-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f9734-120">-Force</span></span>
<span data-ttu-id="f9734-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f9734-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9734-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f9734-122">-Name</span></span>
<span data-ttu-id="f9734-123">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f9734-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f9734-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9734-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9734-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f9734-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f9734-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f9734-126">-Confirm</span></span>
<span data-ttu-id="f9734-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f9734-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9734-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9734-128">-WhatIf</span></span>
<span data-ttu-id="f9734-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9734-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9734-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9734-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9734-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9734-131">CommonParameters</span></span>
<span data-ttu-id="f9734-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9734-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9734-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9734-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9734-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9734-134">INPUTS</span></span>

### <span data-ttu-id="f9734-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f9734-135">System.String</span></span>

## <span data-ttu-id="f9734-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9734-136">OUTPUTS</span></span>

### <span data-ttu-id="f9734-137">System. void</span><span class="sxs-lookup"><span data-stu-id="f9734-137">System.Void</span></span>

## <span data-ttu-id="f9734-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9734-138">NOTES</span></span>

## <span data-ttu-id="f9734-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9734-139">RELATED LINKS</span></span>

[<span data-ttu-id="f9734-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f9734-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="f9734-141">Neu – AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f9734-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="f9734-142">Satz-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f9734-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


