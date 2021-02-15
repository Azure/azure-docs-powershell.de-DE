---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166620"
---
# <span data-ttu-id="31817-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="31817-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="31817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31817-102">SYNOPSIS</span></span>
<span data-ttu-id="31817-103">Holen Sie sich die Zugriffstasten der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="31817-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="31817-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31817-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="31817-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31817-105">DESCRIPTION</span></span>
<span data-ttu-id="31817-106">Holen Sie sich die Zugriffstasten der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="31817-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="31817-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="31817-107">EXAMPLES</span></span>

### <span data-ttu-id="31817-108">Beispiel 1: Abrufen des Schlüssels für den angegebenen Kommunikationsdienst</span><span class="sxs-lookup"><span data-stu-id="31817-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="31817-109">Zeigt die ConnectionString und den Schlüssel für den angegebenen Kommunikationsdienst an.</span><span class="sxs-lookup"><span data-stu-id="31817-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="31817-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31817-110">PARAMETERS</span></span>

### <span data-ttu-id="31817-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="31817-111">-CommunicationServiceName</span></span>
<span data-ttu-id="31817-112">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="31817-112">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31817-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31817-113">-DefaultProfile</span></span>
<span data-ttu-id="31817-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31817-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31817-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31817-115">-ResourceGroupName</span></span>
<span data-ttu-id="31817-116">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="31817-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="31817-117">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="31817-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31817-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31817-118">-SubscriptionId</span></span>
<span data-ttu-id="31817-119">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="31817-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="31817-120">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="31817-120">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31817-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31817-121">-Confirm</span></span>
<span data-ttu-id="31817-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31817-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31817-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="31817-123">-WhatIf</span></span>
<span data-ttu-id="31817-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31817-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31817-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31817-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31817-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31817-126">CommonParameters</span></span>
<span data-ttu-id="31817-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31817-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31817-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31817-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31817-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="31817-129">INPUTS</span></span>

## <span data-ttu-id="31817-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="31817-130">OUTPUTS</span></span>

### <span data-ttu-id="31817-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="31817-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="31817-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="31817-132">NOTES</span></span>

<span data-ttu-id="31817-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="31817-133">ALIASES</span></span>

## <span data-ttu-id="31817-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="31817-134">RELATED LINKS</span></span>

