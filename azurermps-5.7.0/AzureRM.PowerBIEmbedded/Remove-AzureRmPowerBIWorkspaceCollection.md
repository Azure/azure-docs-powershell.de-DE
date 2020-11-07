---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7f3a48db5d8f1e6c7b4b0e73b705fc375a0b514f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664225"
---
# <span data-ttu-id="9abb9-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9abb9-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="9abb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9abb9-102">SYNOPSIS</span></span>
<span data-ttu-id="9abb9-103">Entfernt eine Power BI-Arbeitsbereichs Sammlung.</span><span class="sxs-lookup"><span data-stu-id="9abb9-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9abb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9abb9-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9abb9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9abb9-105">DESCRIPTION</span></span>
<span data-ttu-id="9abb9-106">Das Cmdlet **Remove-AzureRmPowerBIWorkspaceCollection** entfernt eine Power BI-Arbeitsbereichs Sammlung aus ihrer Azure-Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9abb9-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="9abb9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9abb9-107">EXAMPLES</span></span>

### <span data-ttu-id="9abb9-108">Beispiel 1: Entfernen einer Arbeitsbereichs Sammlung</span><span class="sxs-lookup"><span data-stu-id="9abb9-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="9abb9-109">Dieser Befehl entfernt die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9abb9-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="9abb9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9abb9-110">PARAMETERS</span></span>

### <span data-ttu-id="9abb9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abb9-111">-DefaultProfile</span></span>
<span data-ttu-id="9abb9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9abb9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9abb9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9abb9-113">-ResourceGroupName</span></span>
<span data-ttu-id="9abb9-114">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet eine arbeitsbereichsauflistung entfernt.</span><span class="sxs-lookup"><span data-stu-id="9abb9-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abb9-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="9abb9-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="9abb9-116">Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9abb9-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9abb9-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9abb9-117">-Confirm</span></span>
<span data-ttu-id="9abb9-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9abb9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abb9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abb9-119">-WhatIf</span></span>
<span data-ttu-id="9abb9-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9abb9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9abb9-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9abb9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abb9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abb9-122">CommonParameters</span></span>
<span data-ttu-id="9abb9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abb9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abb9-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9abb9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abb9-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9abb9-125">INPUTS</span></span>

### <span data-ttu-id="9abb9-126">Keine</span><span class="sxs-lookup"><span data-stu-id="9abb9-126">None</span></span>
<span data-ttu-id="9abb9-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9abb9-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9abb9-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9abb9-128">OUTPUTS</span></span>

## <span data-ttu-id="9abb9-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="9abb9-129">NOTES</span></span>

## <span data-ttu-id="9abb9-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9abb9-130">RELATED LINKS</span></span>

[<span data-ttu-id="9abb9-131">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9abb9-131">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="9abb9-132">Neu – AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="9abb9-132">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


