---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 98830e2dbcfc115cd026c33782030bc40fa6763f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300323"
---
# <span data-ttu-id="5a96c-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a96c-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="5a96c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a96c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a96c-103">Erstellt eine neue private DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="5a96c-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="5a96c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a96c-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a96c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a96c-105">DESCRIPTION</span></span>
<span data-ttu-id="5a96c-106">Das **Cmdlet "New-AzPrivateDnsZone"** erstellt eine neue Private Domain Name System (DNS)-Zone in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a96c-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="5a96c-107">Sie müssen einen eindeutigen namen der privaten DNS-Zone für den *Parameter "Name"* angeben, da das Cmdlet einen Fehler zurück gibt.</span><span class="sxs-lookup"><span data-stu-id="5a96c-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="5a96c-108">Nachdem die Zone erstellt wurde, verwenden Sie das New-AzPrivateDnsRecordSet-Cmdlet, um Datensatzsätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5a96c-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="5a96c-109">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="5a96c-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="5a96c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5a96c-110">EXAMPLES</span></span>

### <span data-ttu-id="5a96c-111">Beispiel 1: Erstellen einer privaten DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="5a96c-111">Example 1: Create a Private DNS zone</span></span>
```
PS C:\>$Zone = New-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"


This command creates a new private DNS zone named myzone.com in the specified resource group, and then
stores it in the $Zone variable. $Zone object looks something like this,

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="5a96c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a96c-112">PARAMETERS</span></span>

### <span data-ttu-id="5a96c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a96c-113">-DefaultProfile</span></span>
<span data-ttu-id="5a96c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5a96c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a96c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5a96c-115">-Name</span></span>
<span data-ttu-id="5a96c-116">Gibt den Namen der privaten ZU erstellenden privaten DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="5a96c-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="5a96c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a96c-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a96c-118">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a96c-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="5a96c-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a96c-119">-Tag</span></span>
<span data-ttu-id="5a96c-120">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a96c-120">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a96c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a96c-121">-Confirm</span></span>
<span data-ttu-id="5a96c-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a96c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a96c-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5a96c-123">-WhatIf</span></span>
<span data-ttu-id="5a96c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a96c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a96c-125">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a96c-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a96c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a96c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a96c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a96c-127">CommonParameters</span></span>
<span data-ttu-id="5a96c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a96c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a96c-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a96c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a96c-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5a96c-130">INPUTS</span></span>

### <span data-ttu-id="5a96c-131">Keine</span><span class="sxs-lookup"><span data-stu-id="5a96c-131">None</span></span>

## <span data-ttu-id="5a96c-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5a96c-132">OUTPUTS</span></span>

### <span data-ttu-id="5a96c-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a96c-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="5a96c-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5a96c-134">NOTES</span></span>

## <span data-ttu-id="5a96c-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5a96c-135">RELATED LINKS</span></span>

[<span data-ttu-id="5a96c-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a96c-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="5a96c-137">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5a96c-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="5a96c-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a96c-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
