---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: f9f4cc86a07c50718511c3ed0889d96f7acec9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938971"
---
# <span data-ttu-id="ac9fa-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="ac9fa-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="ac9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9fa-103">Holen Sie sich den CommunicationService und seine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="ac9fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac9fa-104">SYNTAX</span></span>

### <span data-ttu-id="ac9fa-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac9fa-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ac9fa-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="ac9fa-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ac9fa-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ac9fa-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac9fa-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="ac9fa-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ac9fa-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac9fa-109">DESCRIPTION</span></span>
<span data-ttu-id="ac9fa-110">Holen Sie sich den CommunicationService und seine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="ac9fa-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac9fa-111">EXAMPLES</span></span>

### <span data-ttu-id="ac9fa-112">Beispiel 1: Auflisten vorhandener CommunicationServices für ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="ac9fa-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="ac9fa-113">Gibt eine Liste aller ACS-Ressourcen unter diesem Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="ac9fa-114">Beispiel 2: Informationen zu angegebenen Azure Communication-Ressourcen erhalten</span><span class="sxs-lookup"><span data-stu-id="ac9fa-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="ac9fa-115">Gibt die Informationen für eine ACS-Ressource zurück, wenn ein übereinstimmender bereitgestellter Parameter gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="ac9fa-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ac9fa-116">PARAMETERS</span></span>

### <span data-ttu-id="ac9fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9fa-117">-DefaultProfile</span></span>
<span data-ttu-id="ac9fa-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9fa-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac9fa-119">-InputObject</span></span>
<span data-ttu-id="ac9fa-120">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac9fa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ac9fa-121">-Name</span></span>
<span data-ttu-id="ac9fa-122">Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9fa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac9fa-123">-ResourceGroupName</span></span>
<span data-ttu-id="ac9fa-124">Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ac9fa-125">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9fa-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac9fa-126">-SubscriptionId</span></span>
<span data-ttu-id="ac9fa-127">Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ac9fa-128">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac9fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9fa-129">CommonParameters</span></span>
<span data-ttu-id="ac9fa-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9fa-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac9fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9fa-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac9fa-132">INPUTS</span></span>

### <span data-ttu-id="ac9fa-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="ac9fa-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="ac9fa-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac9fa-134">OUTPUTS</span></span>

### <span data-ttu-id="ac9fa-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="ac9fa-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="ac9fa-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ac9fa-136">NOTES</span></span>

<span data-ttu-id="ac9fa-137">ALIASE</span><span class="sxs-lookup"><span data-stu-id="ac9fa-137">ALIASES</span></span>

<span data-ttu-id="ac9fa-138">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="ac9fa-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac9fa-139">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac9fa-140">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac9fa-141">INPUTOBJECT <ICommunicationIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="ac9fa-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac9fa-142">`[CommunicationServiceName <String>]`: Der Name der CommunicationService-Ressource.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="ac9fa-143">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="ac9fa-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac9fa-144">`[Location <String>]`: Die Azure-Region</span><span class="sxs-lookup"><span data-stu-id="ac9fa-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="ac9fa-145">`[OperationId <String>]`: Die ID eines laufenden asynchronen Vorgangs</span><span class="sxs-lookup"><span data-stu-id="ac9fa-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="ac9fa-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ac9fa-147">Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ac9fa-148">`[SubscriptionId <String>]`: Ruft die Abonnement-ID ab, die das Microsoft Azure-Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="ac9fa-149">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="ac9fa-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ac9fa-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ac9fa-150">RELATED LINKS</span></span>

