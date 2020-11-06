---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c7beab54a416809a3f5edd033d4c7946a16b807b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504034"
---
# <span data-ttu-id="25505-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="25505-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="25505-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25505-102">SYNOPSIS</span></span>
<span data-ttu-id="25505-103">Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichs Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="25505-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25505-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25505-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25505-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25505-105">DESCRIPTION</span></span>
<span data-ttu-id="25505-106">Das Cmdlet " **Get-AzureRmPowerBIWorkspace** " Ruft die Arbeitsbereiche in einer Power BI-Arbeitsbereichs Sammlung ab.</span><span class="sxs-lookup"><span data-stu-id="25505-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="25505-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25505-107">EXAMPLES</span></span>

### <span data-ttu-id="25505-108">Beispiel 1: Abrufen von Arbeitsbereichen einer Arbeitsbereichs Sammlung</span><span class="sxs-lookup"><span data-stu-id="25505-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="25505-109">Dieser Befehl ruft die Arbeitsbereiche ab, die der Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe angehören.</span><span class="sxs-lookup"><span data-stu-id="25505-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="25505-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25505-110">PARAMETERS</span></span>

### <span data-ttu-id="25505-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25505-111">-ResourceGroupName</span></span>
<span data-ttu-id="25505-112">Gibt den Namen der Ressourcengruppe an, zu der die Arbeitsbereichs Sammlung gehört.</span><span class="sxs-lookup"><span data-stu-id="25505-112">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="25505-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="25505-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="25505-114">Gibt den Namen der Arbeitsbereichs Sammlung an, für die dieses Cmdlet Arbeitsbereiche abruft.</span><span class="sxs-lookup"><span data-stu-id="25505-114">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="25505-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25505-115">-DefaultProfile</span></span>
<span data-ttu-id="25505-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25505-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25505-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25505-117">CommonParameters</span></span>
<span data-ttu-id="25505-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25505-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25505-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25505-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25505-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25505-120">INPUTS</span></span>

## <span data-ttu-id="25505-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25505-121">OUTPUTS</span></span>

### <span data-ttu-id="25505-122">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="25505-122">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="25505-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="25505-123">NOTES</span></span>

## <span data-ttu-id="25505-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25505-124">RELATED LINKS</span></span>

[<span data-ttu-id="25505-125">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="25505-125">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


