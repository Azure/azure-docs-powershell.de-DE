---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 058a914540cd03bcf523f0300e18299c3cf084ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660010"
---
# <span data-ttu-id="4b9ab-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="4b9ab-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="4b9ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b9ab-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9ab-103">Entfernt eine Power BI-Arbeitsbereichs Sammlung.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="4b9ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b9ab-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b9ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b9ab-105">DESCRIPTION</span></span>
<span data-ttu-id="4b9ab-106">Das Cmdlet **Remove-AzPowerBIWorkspaceCollection** entfernt eine Power BI-Arbeitsbereichs Sammlung aus ihrer Azure-Abonnement-und Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="4b9ab-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b9ab-107">EXAMPLES</span></span>

### <span data-ttu-id="4b9ab-108">Beispiel 1: Entfernen einer Arbeitsbereichs Sammlung</span><span class="sxs-lookup"><span data-stu-id="4b9ab-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="4b9ab-109">Dieser Befehl entfernt die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="4b9ab-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b9ab-110">PARAMETERS</span></span>

### <span data-ttu-id="4b9ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b9ab-111">-DefaultProfile</span></span>
<span data-ttu-id="4b9ab-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4b9ab-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b9ab-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b9ab-113">-ResourceGroupName</span></span>
<span data-ttu-id="4b9ab-114">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet eine arbeitsbereichsauflistung entfernt.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="4b9ab-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="4b9ab-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="4b9ab-116">Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4b9ab-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b9ab-117">-Confirm</span></span>
<span data-ttu-id="4b9ab-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b9ab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b9ab-119">-WhatIf</span></span>
<span data-ttu-id="4b9ab-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b9ab-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b9ab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9ab-122">CommonParameters</span></span>
<span data-ttu-id="4b9ab-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b9ab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9ab-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b9ab-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9ab-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b9ab-125">INPUTS</span></span>

### <span data-ttu-id="4b9ab-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4b9ab-126">System.String</span></span>

## <span data-ttu-id="4b9ab-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b9ab-127">OUTPUTS</span></span>

### <span data-ttu-id="4b9ab-128">System. void</span><span class="sxs-lookup"><span data-stu-id="4b9ab-128">System.Void</span></span>

## <span data-ttu-id="4b9ab-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b9ab-129">NOTES</span></span>

## <span data-ttu-id="4b9ab-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b9ab-130">RELATED LINKS</span></span>

[<span data-ttu-id="4b9ab-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="4b9ab-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="4b9ab-132">Neu – AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="4b9ab-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


