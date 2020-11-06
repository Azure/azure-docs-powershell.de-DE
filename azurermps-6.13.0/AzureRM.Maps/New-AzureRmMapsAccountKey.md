---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
ms.openlocfilehash: 13364cde6799a6d99bcdba1d5cd2078c3392a2cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497350"
---
# <span data-ttu-id="b4c00-101">New-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4c00-101">New-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="b4c00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4c00-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c00-103">Generiert einen Kontoschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="b4c00-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4c00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4c00-104">SYNTAX</span></span>

### <span data-ttu-id="b4c00-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4c00-105">NameParameterSet (Default)</span></span>
```
New-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4c00-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4c00-106">InputObjectParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4c00-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4c00-107">ResourceIdParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4c00-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4c00-108">DESCRIPTION</span></span>
<span data-ttu-id="b4c00-109">Das New-AzureRmMapsAccountKey-Cmdlet generiert einen API-Schlüssel für ein Azure Maps-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="b4c00-109">The New-AzureRmMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="b4c00-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4c00-110">EXAMPLES</span></span>

### <span data-ttu-id="b4c00-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4c00-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="b4c00-112">Generiert den primären API-Schlüssel für das Konto "Mein Konto" in der Ressourcengruppe "myresourcegroup" neu.</span><span class="sxs-lookup"><span data-stu-id="b4c00-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="b4c00-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b4c00-113">Example 2</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="b4c00-114">Generiert den sekundären API-Schlüssel für das angegebene Azure Maps-Konto erneut.</span><span class="sxs-lookup"><span data-stu-id="b4c00-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="b4c00-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4c00-115">PARAMETERS</span></span>

### <span data-ttu-id="b4c00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c00-116">-DefaultProfile</span></span>
<span data-ttu-id="b4c00-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4c00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4c00-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4c00-118">-InputObject</span></span>
<span data-ttu-id="b4c00-119">Kartenkonto, das von Get-AzureRmMapsAccount umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="b4c00-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="b4c00-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b4c00-120">-KeyName</span></span>
<span data-ttu-id="b4c00-121">Karten-Kontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="b4c00-121">Maps Account Key.</span></span>

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

### <span data-ttu-id="b4c00-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b4c00-122">-Name</span></span>
<span data-ttu-id="b4c00-123">Ordnet den Kontonamen zu.</span><span class="sxs-lookup"><span data-stu-id="b4c00-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="b4c00-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c00-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4c00-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4c00-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4c00-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b4c00-126">-ResourceId</span></span>
<span data-ttu-id="b4c00-127">Maps-Konto-wiederherkunfts-Nr.</span><span class="sxs-lookup"><span data-stu-id="b4c00-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="b4c00-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4c00-128">-Confirm</span></span>
<span data-ttu-id="b4c00-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4c00-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4c00-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4c00-130">-WhatIf</span></span>
<span data-ttu-id="b4c00-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4c00-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4c00-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4c00-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4c00-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c00-133">CommonParameters</span></span>
<span data-ttu-id="b4c00-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4c00-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c00-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4c00-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c00-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4c00-136">INPUTS</span></span>

### <span data-ttu-id="b4c00-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b4c00-137">System.String</span></span>

### <span data-ttu-id="b4c00-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b4c00-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="b4c00-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b4c00-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b4c00-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4c00-140">OUTPUTS</span></span>

### <span data-ttu-id="b4c00-141">Microsoft. Azure. Management. Maps. Models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b4c00-141">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="b4c00-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4c00-142">NOTES</span></span>

## <span data-ttu-id="b4c00-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4c00-143">RELATED LINKS</span></span>
