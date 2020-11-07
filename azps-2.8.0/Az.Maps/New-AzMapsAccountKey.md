---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: 68a03059a99c8e50d5f0ae77b131fa8ab9ed6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650617"
---
# <span data-ttu-id="42c76-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="42c76-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="42c76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42c76-102">SYNOPSIS</span></span>
<span data-ttu-id="42c76-103">Generiert einen Kontoschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="42c76-103">Regenerates an account key.</span></span>

## <span data-ttu-id="42c76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42c76-104">SYNTAX</span></span>

### <span data-ttu-id="42c76-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="42c76-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42c76-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42c76-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42c76-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42c76-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c76-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42c76-108">DESCRIPTION</span></span>
<span data-ttu-id="42c76-109">Das New-AzMapsAccountKey-Cmdlet generiert einen API-Schlüssel für ein Azure Maps-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="42c76-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="42c76-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42c76-110">EXAMPLES</span></span>

### <span data-ttu-id="42c76-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42c76-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="42c76-112">Generiert den primären API-Schlüssel für das Konto "Mein Konto" in der Ressourcengruppe "myresourcegroup" neu.</span><span class="sxs-lookup"><span data-stu-id="42c76-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="42c76-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="42c76-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="42c76-114">Generiert den sekundären API-Schlüssel für das angegebene Azure Maps-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="42c76-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="42c76-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="42c76-115">PARAMETERS</span></span>

### <span data-ttu-id="42c76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c76-116">-DefaultProfile</span></span>
<span data-ttu-id="42c76-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42c76-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c76-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42c76-118">-InputObject</span></span>
<span data-ttu-id="42c76-119">Kartenkonto, das von Get-AzMapsAccount umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="42c76-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c76-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="42c76-120">-KeyName</span></span>
<span data-ttu-id="42c76-121">Karten-Kontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="42c76-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c76-122">-Name</span><span class="sxs-lookup"><span data-stu-id="42c76-122">-Name</span></span>
<span data-ttu-id="42c76-123">Ordnet den Kontonamen zu.</span><span class="sxs-lookup"><span data-stu-id="42c76-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c76-124">-ResourceGroupName</span></span>
<span data-ttu-id="42c76-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42c76-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c76-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="42c76-126">-ResourceId</span></span>
<span data-ttu-id="42c76-127">Maps-Konto-wiederherkunfts-Nr.</span><span class="sxs-lookup"><span data-stu-id="42c76-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c76-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42c76-128">-Confirm</span></span>
<span data-ttu-id="42c76-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42c76-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c76-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c76-130">-WhatIf</span></span>
<span data-ttu-id="42c76-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42c76-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c76-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42c76-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c76-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c76-133">CommonParameters</span></span>
<span data-ttu-id="42c76-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c76-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c76-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c76-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c76-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42c76-136">INPUTS</span></span>

### <span data-ttu-id="42c76-137">System. String</span><span class="sxs-lookup"><span data-stu-id="42c76-137">System.String</span></span>

### <span data-ttu-id="42c76-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="42c76-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="42c76-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42c76-139">OUTPUTS</span></span>

### <span data-ttu-id="42c76-140">Microsoft. Azure. Management. Maps. Models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="42c76-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="42c76-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="42c76-141">NOTES</span></span>

## <span data-ttu-id="42c76-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42c76-142">RELATED LINKS</span></span>
