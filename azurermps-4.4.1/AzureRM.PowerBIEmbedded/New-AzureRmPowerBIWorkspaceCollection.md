---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 981daec060f47a88b31454cd8d13711091bedcf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504029"
---
# <span data-ttu-id="78854-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="78854-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="78854-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="78854-102">SYNOPSIS</span></span>
<span data-ttu-id="78854-103">Erstellt eine Power BI-Arbeitsbereichs Sammlung.</span><span class="sxs-lookup"><span data-stu-id="78854-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78854-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="78854-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78854-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78854-105">DESCRIPTION</span></span>
<span data-ttu-id="78854-106">Das Cmdlet **New-AzureRmPowerBIWorkspaceCollection** erstellt eine Power BI-Arbeitsbereichs Sammlung für Ihr Azure-Abonnement in der angegebenen Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="78854-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="78854-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78854-107">EXAMPLES</span></span>

### <span data-ttu-id="78854-108">Beispiel 1: Erstellen einer Arbeitsbereichs Sammlung</span><span class="sxs-lookup"><span data-stu-id="78854-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="78854-109">Dieser Befehl erstellt eine Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="78854-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="78854-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="78854-110">PARAMETERS</span></span>

### <span data-ttu-id="78854-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="78854-111">-Location</span></span>
<span data-ttu-id="78854-112">Gibt den Azure-Speicherort an, an dem dieses Cmdlet eine Arbeitsbereichs Sammlung erstellt.</span><span class="sxs-lookup"><span data-stu-id="78854-112">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="78854-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78854-113">-ResourceGroupName</span></span>
<span data-ttu-id="78854-114">Gibt den Namen der Ressourcengruppe an, in der mit diesem Cmdlet eine Arbeitsbereichs Sammlung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="78854-114">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="78854-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="78854-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="78854-116">Gibt einen Namen für die Power BI-Arbeitsbereichs Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="78854-116">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="78854-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="78854-117">-Confirm</span></span>
<span data-ttu-id="78854-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78854-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78854-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78854-119">-WhatIf</span></span>
<span data-ttu-id="78854-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78854-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78854-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78854-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78854-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78854-122">-DefaultProfile</span></span>
<span data-ttu-id="78854-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="78854-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78854-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78854-124">CommonParameters</span></span>
<span data-ttu-id="78854-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78854-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78854-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78854-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78854-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="78854-127">INPUTS</span></span>

## <span data-ttu-id="78854-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="78854-128">OUTPUTS</span></span>

### <span data-ttu-id="78854-129">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="78854-129">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="78854-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="78854-130">NOTES</span></span>

## <span data-ttu-id="78854-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="78854-131">RELATED LINKS</span></span>

[<span data-ttu-id="78854-132">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="78854-132">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="78854-133">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="78854-133">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


