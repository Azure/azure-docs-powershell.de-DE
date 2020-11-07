---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 35287cf75c8fbcb726ace19abe6f7c6923b537df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663344"
---
# <span data-ttu-id="b586f-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b586f-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="b586f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b586f-102">SYNOPSIS</span></span>
<span data-ttu-id="b586f-103">Entfernt eine Power BI-Arbeitsbereichs Sammlung.</span><span class="sxs-lookup"><span data-stu-id="b586f-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b586f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b586f-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b586f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b586f-105">DESCRIPTION</span></span>
<span data-ttu-id="b586f-106">Das Cmdlet **Remove-AzureRmPowerBIWorkspaceCollection** entfernt eine Power BI-Arbeitsbereichs Sammlung aus ihrer Azure-Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b586f-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="b586f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b586f-107">EXAMPLES</span></span>

### <span data-ttu-id="b586f-108">Beispiel 1: Entfernen einer Arbeitsbereichs Sammlung</span><span class="sxs-lookup"><span data-stu-id="b586f-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="b586f-109">Dieser Befehl entfernt die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b586f-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b586f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b586f-110">PARAMETERS</span></span>

### <span data-ttu-id="b586f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b586f-111">-DefaultProfile</span></span>
<span data-ttu-id="b586f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b586f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b586f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b586f-113">-ResourceGroupName</span></span>
<span data-ttu-id="b586f-114">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet eine arbeitsbereichsauflistung entfernt.</span><span class="sxs-lookup"><span data-stu-id="b586f-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="b586f-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b586f-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b586f-116">Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b586f-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b586f-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b586f-117">-Confirm</span></span>
<span data-ttu-id="b586f-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b586f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b586f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b586f-119">-WhatIf</span></span>
<span data-ttu-id="b586f-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b586f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b586f-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b586f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b586f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b586f-122">CommonParameters</span></span>
<span data-ttu-id="b586f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b586f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b586f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b586f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b586f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b586f-125">INPUTS</span></span>

### <span data-ttu-id="b586f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b586f-126">System.String</span></span>

## <span data-ttu-id="b586f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b586f-127">OUTPUTS</span></span>

### <span data-ttu-id="b586f-128">System. void</span><span class="sxs-lookup"><span data-stu-id="b586f-128">System.Void</span></span>

## <span data-ttu-id="b586f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b586f-129">NOTES</span></span>

## <span data-ttu-id="b586f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b586f-130">RELATED LINKS</span></span>

[<span data-ttu-id="b586f-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b586f-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="b586f-132">Neu – AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="b586f-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


