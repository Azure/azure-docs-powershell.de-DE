---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 71c910fafea0c555f5ba0d7a62573c2de2be3b41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501801"
---
# <span data-ttu-id="c67fa-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c67fa-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="c67fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c67fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c67fa-103">Entfernt ein Integrations Kontozertifikat aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c67fa-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c67fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c67fa-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c67fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c67fa-105">DESCRIPTION</span></span>
<span data-ttu-id="c67fa-106">Das Cmdlet **Remove-AzureRmIntegrationAccountCertificate** entfernt ein Integrations Kontozertifikat aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c67fa-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="c67fa-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="c67fa-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="c67fa-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="c67fa-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c67fa-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="c67fa-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c67fa-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c67fa-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c67fa-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c67fa-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c67fa-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c67fa-112">EXAMPLES</span></span>

### <span data-ttu-id="c67fa-113">Beispiel 1: Entfernen eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="c67fa-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="c67fa-114">Mit diesem Befehl wird das Integrations Kontozertifikat mit dem Namen IntegrationAccount31 entfernt.</span><span class="sxs-lookup"><span data-stu-id="c67fa-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="c67fa-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c67fa-115">PARAMETERS</span></span>

### <span data-ttu-id="c67fa-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c67fa-116">-CertificateName</span></span>
<span data-ttu-id="c67fa-117">Gibt den Namen eines Integrations Kontozertifikats an.</span><span class="sxs-lookup"><span data-stu-id="c67fa-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="c67fa-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c67fa-118">-Force</span></span>
<span data-ttu-id="c67fa-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c67fa-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c67fa-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c67fa-120">-Name</span></span>
<span data-ttu-id="c67fa-121">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="c67fa-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="c67fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c67fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="c67fa-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c67fa-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c67fa-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c67fa-124">-Confirm</span></span>
<span data-ttu-id="c67fa-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c67fa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c67fa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c67fa-126">-WhatIf</span></span>
<span data-ttu-id="c67fa-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c67fa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c67fa-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c67fa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c67fa-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c67fa-129">-DefaultProfile</span></span>
<span data-ttu-id="c67fa-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c67fa-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c67fa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c67fa-131">CommonParameters</span></span>
<span data-ttu-id="c67fa-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c67fa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c67fa-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c67fa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c67fa-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c67fa-134">INPUTS</span></span>

## <span data-ttu-id="c67fa-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c67fa-135">OUTPUTS</span></span>

## <span data-ttu-id="c67fa-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="c67fa-136">NOTES</span></span>

## <span data-ttu-id="c67fa-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c67fa-137">RELATED LINKS</span></span>

[<span data-ttu-id="c67fa-138">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c67fa-138">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="c67fa-139">Neu – AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c67fa-139">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="c67fa-140">Satz-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c67fa-140">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


