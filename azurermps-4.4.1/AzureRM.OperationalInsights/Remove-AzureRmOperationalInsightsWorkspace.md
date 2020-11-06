---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 3f7ed1a36cc95296ee7fdeec45c5039063032d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479006"
---
# <span data-ttu-id="a47d4-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a47d4-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="a47d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a47d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a47d4-103">Entfernt einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a47d4-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a47d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a47d4-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a47d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a47d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a47d4-106">Das Cmdlet **Remove-AzureRmOperationalInsightsWorkspace** löscht einen vorhandenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a47d4-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="a47d4-107">Wenn dieser Arbeitsbereich mit einem vorhandenen Konto über den *CustomerID* -Parameter zum Zeitpunkt der Erstellung verknüpft wurde, wird das ursprüngliche Konto nicht im Portal "operative Einblicke" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a47d4-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="a47d4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a47d4-108">EXAMPLES</span></span>

### <span data-ttu-id="a47d4-109">Beispiel 1: Entfernen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="a47d4-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="a47d4-110">Mit diesem Befehl wird der Arbeitsbereich mit dem Namen "myworkspace" aus der Ressourcengruppe "ContosoResourceGroup" entfernt.</span><span class="sxs-lookup"><span data-stu-id="a47d4-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="a47d4-111">Beispiel 2: Entfernen eines Arbeitsbereichs mithilfe der Pipeline und ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="a47d4-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="a47d4-112">Dieser Befehl verwendet das Get-AzureRmOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen "myworkspace" abzurufen, und übergibt ihn dann mithilfe des Pipelineoperators an das Cmdlet " **Remove-AzureRmOperationalInsightsWorkspace** ", um ihn zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a47d4-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="a47d4-113">Da der Parameter *Force* angegeben ist, werden Sie nicht vom Befehl aufgefordert, bevor Sie den Arbeitsbereich entfernen.</span><span class="sxs-lookup"><span data-stu-id="a47d4-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="a47d4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a47d4-114">PARAMETERS</span></span>

### <span data-ttu-id="a47d4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a47d4-115">-Force</span></span>
<span data-ttu-id="a47d4-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a47d4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a47d4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a47d4-117">-Name</span></span>
<span data-ttu-id="a47d4-118">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="a47d4-118">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a47d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="a47d4-120">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a47d4-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a47d4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a47d4-121">-Confirm</span></span>
<span data-ttu-id="a47d4-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a47d4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a47d4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a47d4-123">-WhatIf</span></span>
<span data-ttu-id="a47d4-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a47d4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a47d4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a47d4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a47d4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47d4-126">-DefaultProfile</span></span>
<span data-ttu-id="a47d4-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a47d4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a47d4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47d4-128">CommonParameters</span></span>
<span data-ttu-id="a47d4-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a47d4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47d4-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a47d4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47d4-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a47d4-131">INPUTS</span></span>

## <span data-ttu-id="a47d4-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a47d4-132">OUTPUTS</span></span>

## <span data-ttu-id="a47d4-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a47d4-133">NOTES</span></span>

## <span data-ttu-id="a47d4-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a47d4-134">RELATED LINKS</span></span>

[<span data-ttu-id="a47d4-135">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="a47d4-135">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="a47d4-136">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a47d4-136">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


