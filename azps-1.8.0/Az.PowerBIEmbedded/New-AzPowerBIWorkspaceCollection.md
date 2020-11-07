---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c16632f621af0dfe3f6b6a1b53148eef2c480e8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660012"
---
# <span data-ttu-id="0db3b-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0db3b-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="0db3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0db3b-102">SYNOPSIS</span></span>
<span data-ttu-id="0db3b-103">Erstellt eine Power BI-Arbeitsbereichs Sammlung.</span><span class="sxs-lookup"><span data-stu-id="0db3b-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="0db3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0db3b-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db3b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0db3b-105">DESCRIPTION</span></span>
<span data-ttu-id="0db3b-106">Das Cmdlet **New-AzPowerBIWorkspaceCollection** erstellt eine Power BI-Arbeitsbereichs Sammlung für Ihr Azure-Abonnement in der angegebenen Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="0db3b-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="0db3b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0db3b-107">EXAMPLES</span></span>

### <span data-ttu-id="0db3b-108">Beispiel 1: Erstellen einer Arbeitsbereichs Sammlung</span><span class="sxs-lookup"><span data-stu-id="0db3b-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="0db3b-109">Dieser Befehl erstellt eine Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="0db3b-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="0db3b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0db3b-110">PARAMETERS</span></span>

### <span data-ttu-id="0db3b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db3b-111">-DefaultProfile</span></span>
<span data-ttu-id="0db3b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0db3b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0db3b-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="0db3b-113">-Location</span></span>
<span data-ttu-id="0db3b-114">Gibt den Azure-Speicherort an, an dem dieses Cmdlet eine Arbeitsbereichs Sammlung erstellt.</span><span class="sxs-lookup"><span data-stu-id="0db3b-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db3b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db3b-115">-ResourceGroupName</span></span>
<span data-ttu-id="0db3b-116">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet eine Arbeitsbereichs Sammlung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0db3b-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="0db3b-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="0db3b-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="0db3b-118">Gibt einen Namen für die Power BI-Arbeitsbereichs Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="0db3b-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="0db3b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0db3b-119">-Confirm</span></span>
<span data-ttu-id="0db3b-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0db3b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db3b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db3b-121">-WhatIf</span></span>
<span data-ttu-id="0db3b-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0db3b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db3b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0db3b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db3b-124">CommonParameters</span></span>
<span data-ttu-id="0db3b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db3b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db3b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db3b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0db3b-127">INPUTS</span></span>

### <span data-ttu-id="0db3b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0db3b-128">System.String</span></span>

## <span data-ttu-id="0db3b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0db3b-129">OUTPUTS</span></span>

### <span data-ttu-id="0db3b-130">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0db3b-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="0db3b-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="0db3b-131">NOTES</span></span>

## <span data-ttu-id="0db3b-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0db3b-132">RELATED LINKS</span></span>

[<span data-ttu-id="0db3b-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0db3b-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="0db3b-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="0db3b-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


