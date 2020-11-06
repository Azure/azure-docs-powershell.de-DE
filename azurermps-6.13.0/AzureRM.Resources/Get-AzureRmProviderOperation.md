---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: ff56fc9df0d2303938700d85323a98575d1fb0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482130"
---
# <span data-ttu-id="e702b-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="e702b-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="e702b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e702b-102">SYNOPSIS</span></span>
<span data-ttu-id="e702b-103">Ruft die Vorgänge für einen Azure-Ressourcenanbieter ab, die mithilfe von Azure RBAC Sicherungs fähig sind.</span><span class="sxs-lookup"><span data-stu-id="e702b-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e702b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e702b-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e702b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e702b-105">DESCRIPTION</span></span>
<span data-ttu-id="e702b-106">Die Get-AzureRmProviderOperation ruft die von Azure-Ressourcen Anbietern verfügbar gemachten Vorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="e702b-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="e702b-107">Vorgänge können zum Erstellen benutzerdefinierter Rollen in Azure RBAC zusammengestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e702b-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="e702b-108">Der Befehl nimmt als Eingabe eine Vorgangs Suchzeichenfolge (mit möglichen Platzhalter \*Zeichen ()) an, die die anzuzeigenden Vorgangsdetails bestimmt. Verwenden Sie Get-AzureRmProviderOperation *, um alle Vorgänge für alle Azure-Ressourcenanbieter abzurufen. Verwenden Sie Get-AzureRmProviderOperation Microsoft. Compute/* , um alle Vorgänge des Microsoft. Compute-Ressourcenanbieters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e702b-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="e702b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e702b-109">EXAMPLES</span></span>

### <span data-ttu-id="e702b-110">Abrufen aller Aktionen für alle Anbieter</span><span class="sxs-lookup"><span data-stu-id="e702b-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="e702b-111">Abrufen von Aktionen für einen bestimmten Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="e702b-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="e702b-112">Abrufen aller Aktionen, die auf virtuellen Computern ausgeführt werden können</span><span class="sxs-lookup"><span data-stu-id="e702b-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="e702b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e702b-113">PARAMETERS</span></span>

### <span data-ttu-id="e702b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e702b-114">-DefaultProfile</span></span>
<span data-ttu-id="e702b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e702b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e702b-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="e702b-116">-OperationSearchString</span></span>
<span data-ttu-id="e702b-117">Die Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen (\*))</span><span class="sxs-lookup"><span data-stu-id="e702b-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="e702b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e702b-118">CommonParameters</span></span>
<span data-ttu-id="e702b-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e702b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e702b-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e702b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e702b-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e702b-121">INPUTS</span></span>

### <span data-ttu-id="e702b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e702b-122">System.String</span></span>
<span data-ttu-id="e702b-123">Parameter: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e702b-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="e702b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e702b-124">OUTPUTS</span></span>

### <span data-ttu-id="e702b-125">Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="e702b-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="e702b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="e702b-126">NOTES</span></span>
<span data-ttu-id="e702b-127">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="e702b-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e702b-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e702b-128">RELATED LINKS</span></span>
