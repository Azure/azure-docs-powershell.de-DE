---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153708"
---
# <span data-ttu-id="66a13-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="66a13-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="66a13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66a13-102">SYNOPSIS</span></span>
<span data-ttu-id="66a13-103">Ruft die Vorgänge für einen Azure-Ressourcenanbieter ab, die mit Azure RBAC sicherungsfähig sind.</span><span class="sxs-lookup"><span data-stu-id="66a13-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="66a13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66a13-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66a13-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66a13-105">DESCRIPTION</span></span>
<span data-ttu-id="66a13-106">Die Get-AzProviderOperation macht die Vorgänge von Azure-Ressourcenanbietern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66a13-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="66a13-107">Vorgänge können erstellt werden, um benutzerdefinierte Rollen in Azure RBAC zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="66a13-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="66a13-108">Der Befehl verwendet als Eingabe eine Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen( ) Zeichen(en), die die anzuzeigende *Vorgangsdetails bestimmt. Verwenden Get-AzProviderOperation \* zum Erhalten aller Vorgänge für alle Azure-Ressourcenanbieter. Verwenden Get-AzProviderOperation Microsoft.Compute/,* um alle Vorgänge des Microsoft.Compute-Ressourcenanbieters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="66a13-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="66a13-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66a13-109">EXAMPLES</span></span>

### <span data-ttu-id="66a13-110">Beispiel 1: Alle Aktionen für alle Anbieter erhalten</span><span class="sxs-lookup"><span data-stu-id="66a13-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="66a13-111">Beispiel 2: Erhalten von Aktionen für einen bestimmten Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="66a13-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="66a13-112">Beispiel 3: Alle Aktionen erhalten, die auf virtuellen Computern ausgeführt werden können</span><span class="sxs-lookup"><span data-stu-id="66a13-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="66a13-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66a13-113">PARAMETERS</span></span>

### <span data-ttu-id="66a13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a13-114">-DefaultProfile</span></span>
<span data-ttu-id="66a13-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="66a13-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66a13-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="66a13-116">-OperationSearchString</span></span>
<span data-ttu-id="66a13-117">Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen (\*) )</span><span class="sxs-lookup"><span data-stu-id="66a13-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66a13-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a13-118">CommonParameters</span></span>
<span data-ttu-id="66a13-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a13-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a13-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66a13-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a13-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66a13-121">INPUTS</span></span>

### <span data-ttu-id="66a13-122">System.String</span><span class="sxs-lookup"><span data-stu-id="66a13-122">System.String</span></span>

## <span data-ttu-id="66a13-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66a13-123">OUTPUTS</span></span>

### <span data-ttu-id="66a13-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="66a13-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="66a13-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="66a13-125">NOTES</span></span>
<span data-ttu-id="66a13-126">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="66a13-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="66a13-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="66a13-127">RELATED LINKS</span></span>
