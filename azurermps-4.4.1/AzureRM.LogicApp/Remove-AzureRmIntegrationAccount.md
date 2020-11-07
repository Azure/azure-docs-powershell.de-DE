---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: eb78395274171f448076a4cd3ad9b6bac0093301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665370"
---
# <span data-ttu-id="b848e-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b848e-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="b848e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b848e-102">SYNOPSIS</span></span>
<span data-ttu-id="b848e-103">Entfernt ein Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="b848e-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b848e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b848e-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b848e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b848e-105">DESCRIPTION</span></span>
<span data-ttu-id="b848e-106">Das Cmdlet **Remove-AzureRmIntegrationAccount** entfernt ein Integrations Konto aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b848e-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="b848e-107">Geben Sie den Namen des Integrations Kontos und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b848e-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="b848e-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="b848e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b848e-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="b848e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b848e-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b848e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b848e-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b848e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b848e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b848e-112">EXAMPLES</span></span>

### <span data-ttu-id="b848e-113">Beispiel 1: Entfernen eines Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="b848e-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="b848e-114">Dieser Befehl entfernt ein Integrations Konto mit dem Namen IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="b848e-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="b848e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b848e-115">PARAMETERS</span></span>

### <span data-ttu-id="b848e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b848e-116">-Force</span></span>
<span data-ttu-id="b848e-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b848e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b848e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b848e-118">-Name</span></span>
<span data-ttu-id="b848e-119">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b848e-119">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b848e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b848e-120">-ResourceGroupName</span></span>
<span data-ttu-id="b848e-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b848e-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b848e-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b848e-122">-Confirm</span></span>
<span data-ttu-id="b848e-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b848e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b848e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b848e-124">-WhatIf</span></span>
<span data-ttu-id="b848e-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b848e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b848e-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b848e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b848e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b848e-127">-DefaultProfile</span></span>
<span data-ttu-id="b848e-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b848e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b848e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b848e-129">CommonParameters</span></span>
<span data-ttu-id="b848e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b848e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b848e-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b848e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b848e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b848e-132">INPUTS</span></span>

## <span data-ttu-id="b848e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b848e-133">OUTPUTS</span></span>

## <span data-ttu-id="b848e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b848e-134">NOTES</span></span>

## <span data-ttu-id="b848e-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b848e-135">RELATED LINKS</span></span>

[<span data-ttu-id="b848e-136">Neu – AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b848e-136">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="b848e-137">Satz-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b848e-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="b848e-138">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b848e-138">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


