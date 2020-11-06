---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 891f7fcd50281f5dab9b8d4eaf9f1bd842fbc85e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479142"
---
# <span data-ttu-id="99dba-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99dba-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="99dba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99dba-102">SYNOPSIS</span></span>
<span data-ttu-id="99dba-103">Ruft eine Logik-App aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="99dba-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99dba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99dba-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99dba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99dba-105">DESCRIPTION</span></span>
<span data-ttu-id="99dba-106">Das Cmdlet " **Get-AzureRmLogicApp** " Ruft eine Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="99dba-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="99dba-107">Dieses Cmdlet gibt ein **Workflow** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="99dba-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="99dba-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="99dba-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="99dba-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="99dba-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="99dba-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="99dba-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="99dba-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="99dba-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="99dba-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99dba-112">EXAMPLES</span></span>

### <span data-ttu-id="99dba-113">Beispiel 1: Abrufen einer Logik-App aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="99dba-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="99dba-114">Dieser Befehl ruft eine Logik-App aus der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="99dba-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="99dba-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="99dba-115">PARAMETERS</span></span>

### <span data-ttu-id="99dba-116">-Name</span><span class="sxs-lookup"><span data-stu-id="99dba-116">-Name</span></span>
<span data-ttu-id="99dba-117">Gibt den Namen der Logik-APP an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="99dba-117">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99dba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99dba-118">-ResourceGroupName</span></span>
<span data-ttu-id="99dba-119">Gibt den Namen für eine Ressourcengruppe an, in der dieses Cmdlet eine Logik-APP erhält.</span><span class="sxs-lookup"><span data-stu-id="99dba-119">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="99dba-120">-Version</span><span class="sxs-lookup"><span data-stu-id="99dba-120">-Version</span></span>
<span data-ttu-id="99dba-121">Gibt die Version einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="99dba-121">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="99dba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99dba-122">-DefaultProfile</span></span>
<span data-ttu-id="99dba-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99dba-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99dba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99dba-124">CommonParameters</span></span>
<span data-ttu-id="99dba-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99dba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99dba-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99dba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99dba-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99dba-127">INPUTS</span></span>

## <span data-ttu-id="99dba-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99dba-128">OUTPUTS</span></span>

### <span data-ttu-id="99dba-129">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="99dba-129">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="99dba-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="99dba-130">NOTES</span></span>

## <span data-ttu-id="99dba-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99dba-131">RELATED LINKS</span></span>

[<span data-ttu-id="99dba-132">Neu – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99dba-132">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="99dba-133">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99dba-133">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="99dba-134">Satz-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99dba-134">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="99dba-135">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99dba-135">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


