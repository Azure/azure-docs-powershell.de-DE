---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301137"
---
# <span data-ttu-id="75090-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="75090-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="75090-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75090-102">SYNOPSIS</span></span>
<span data-ttu-id="75090-103">Ruft die Vorgänge für einen Azure-Ressourcenanbieter ab, die mithilfe von Azure RBAC Sicherungs fähig sind.</span><span class="sxs-lookup"><span data-stu-id="75090-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="75090-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75090-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75090-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75090-105">DESCRIPTION</span></span>
<span data-ttu-id="75090-106">Die Get-AzProviderOperation ruft die von Azure-Ressourcen Anbietern verfügbar gemachten Vorgänge ab.</span><span class="sxs-lookup"><span data-stu-id="75090-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="75090-107">Vorgänge können zum Erstellen benutzerdefinierter Rollen in Azure RBAC zusammengestellt werden.</span><span class="sxs-lookup"><span data-stu-id="75090-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="75090-108">Der Befehl nimmt als Eingabe eine Vorgangs Suchzeichenfolge (mit möglichen Platzhalter \*Zeichen ()) an, die die anzuzeigenden Vorgangsdetails bestimmt. Verwenden Sie Get-AzProviderOperation *, um alle Vorgänge für alle Azure-Ressourcenanbieter abzurufen. Verwenden Sie Get-AzProviderOperation Microsoft. Compute/* , um alle Vorgänge des Microsoft. Compute-Ressourcenanbieters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="75090-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="75090-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75090-109">EXAMPLES</span></span>

### <span data-ttu-id="75090-110">Beispiel 1: Abrufen aller Aktionen für alle Anbieter</span><span class="sxs-lookup"><span data-stu-id="75090-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="75090-111">Beispiel 2: Abrufen von Aktionen für einen bestimmten Ressourcenanbieter</span><span class="sxs-lookup"><span data-stu-id="75090-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="75090-112">Beispiel 3: Abrufen aller Aktionen, die auf virtuellen Computern ausgeführt werden können</span><span class="sxs-lookup"><span data-stu-id="75090-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="75090-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="75090-113">PARAMETERS</span></span>

### <span data-ttu-id="75090-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75090-114">-DefaultProfile</span></span>
<span data-ttu-id="75090-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="75090-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75090-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="75090-116">-OperationSearchString</span></span>
<span data-ttu-id="75090-117">Die Suchzeichenfolge des Vorgangs (mit möglichen Platzhalterzeichen (\*))</span><span class="sxs-lookup"><span data-stu-id="75090-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="75090-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75090-118">CommonParameters</span></span>
<span data-ttu-id="75090-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75090-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75090-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75090-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75090-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75090-121">INPUTS</span></span>

### <span data-ttu-id="75090-122">System. String</span><span class="sxs-lookup"><span data-stu-id="75090-122">System.String</span></span>

## <span data-ttu-id="75090-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75090-123">OUTPUTS</span></span>

### <span data-ttu-id="75090-124">Microsoft. Azure. Commands. resources. Models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="75090-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="75090-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="75090-125">NOTES</span></span>
<span data-ttu-id="75090-126">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="75090-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="75090-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75090-127">RELATED LINKS</span></span>
