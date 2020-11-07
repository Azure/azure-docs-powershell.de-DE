---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 811a69b8d18c5e723702f73873188961f2739360
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/22/2020
ms.locfileid: "93851099"
---
# <span data-ttu-id="275da-101">Get-AzsAzureBridgeActivation</span><span class="sxs-lookup"><span data-stu-id="275da-101">Get-AzsAzureBridgeActivation</span></span>

## <span data-ttu-id="275da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="275da-102">SYNOPSIS</span></span>
<span data-ttu-id="275da-103">Gibt die Azure Bridge-Aktivierung zurück.</span><span class="sxs-lookup"><span data-stu-id="275da-103">Returns the Azure Bridge Activation.</span></span>

## <span data-ttu-id="275da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="275da-104">SYNTAX</span></span>

### <span data-ttu-id="275da-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="275da-105">List (Default)</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="275da-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="275da-106">Get</span></span>
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="275da-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="275da-107">ResourceId</span></span>
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="275da-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="275da-108">DESCRIPTION</span></span>
<span data-ttu-id="275da-109">Sobald Azure Stack registriert wurde, enthält das Aktivierungsobjekt Informationen, die eine Azure Stack-Bereitstellung mit Ihrer Registrierung in Azure verknüpft, beispielsweise das Ablaufdatum der Registrierung, den Namen usw.</span><span class="sxs-lookup"><span data-stu-id="275da-109">Once Azure Stack has been registered, the activation object contains information that links an Azure Stack deployment to its registration in Azure, for example, the registration expiration date, name, etc.</span></span>

## <span data-ttu-id="275da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="275da-110">EXAMPLES</span></span>

### <span data-ttu-id="275da-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="275da-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

<span data-ttu-id="275da-112">Abrufen einer Liste der Azure Bridge-Aktivierungen unter der Ressourcengruppe "activationRG"</span><span class="sxs-lookup"><span data-stu-id="275da-112">Get a list of Azure Bridge Activations under the resource group "activationRG"</span></span>

### <span data-ttu-id="275da-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="275da-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

<span data-ttu-id="275da-114">Besorgen Sie sich eine Azure Bridge-Aktivierung mit dem Namen "myactivation" unter "activationRG"</span><span class="sxs-lookup"><span data-stu-id="275da-114">Get an Azure Bridge Activation by name 'myActivation' situated under 'activationRG'</span></span>

## <span data-ttu-id="275da-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="275da-115">PARAMETERS</span></span>

### <span data-ttu-id="275da-116">-Name</span><span class="sxs-lookup"><span data-stu-id="275da-116">-Name</span></span>
<span data-ttu-id="275da-117">Der Name der Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="275da-117">Name of the activation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275da-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275da-118">-ResourceGroupName</span></span>
<span data-ttu-id="275da-119">Die während der Registrierung von Azure Stack verwendete Ressourcengruppe; Sie können auch Ressourcengruppennamen im Portal anzeigen.</span><span class="sxs-lookup"><span data-stu-id="275da-119">The Resource Group used during the registration of Azure Stack; you can also view Resource Group names in the portal.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275da-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="275da-120">-ResourceId</span></span>
<span data-ttu-id="275da-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="275da-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275da-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="275da-122">-Skip</span></span>
<span data-ttu-id="275da-123">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="275da-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275da-124">-Top</span><span class="sxs-lookup"><span data-stu-id="275da-124">-Top</span></span>
<span data-ttu-id="275da-125">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="275da-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="275da-126">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="275da-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275da-127">CommonParameters</span></span>
<span data-ttu-id="275da-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275da-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275da-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275da-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="275da-130">INPUTS</span></span>

## <span data-ttu-id="275da-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="275da-131">OUTPUTS</span></span>

### <span data-ttu-id="275da-132">Microsoft. AzureStack. Management. AzureBridge. admin. Models. ActivationResource</span><span class="sxs-lookup"><span data-stu-id="275da-132">Microsoft.AzureStack.Management.AzureBridge.Admin.Models.ActivationResource</span></span>

## <span data-ttu-id="275da-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="275da-133">NOTES</span></span>

## <span data-ttu-id="275da-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="275da-134">RELATED LINKS</span></span>

