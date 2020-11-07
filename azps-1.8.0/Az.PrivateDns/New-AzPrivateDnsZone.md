---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsZone.md
ms.openlocfilehash: 20922936f754f18d2ee26631dc616d9723cdc5e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659988"
---
# <span data-ttu-id="c3fb5-101">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="c3fb5-101">New-AzPrivateDnsZone</span></span>

## <span data-ttu-id="c3fb5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="c3fb5-103">Erstellt eine neue private DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-103">Creates a new private DNS zone.</span></span>

## <span data-ttu-id="c3fb5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3fb5-104">SYNTAX</span></span>

```
New-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3fb5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3fb5-105">DESCRIPTION</span></span>
<span data-ttu-id="c3fb5-106">Das Cmdlet **New-AzPrivateDnsZone** erstellt eine neue Private Domain Name System (DNS)-Zone in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-106">The **New-AzPrivateDnsZone** cmdlet creates a new private Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="c3fb5-107">Sie müssen einen eindeutigen privaten DNS-Zonennamen für den Parameter *Name* angeben, oder das Cmdlet gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-107">You must specify a unique private DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="c3fb5-108">Verwenden Sie nach der Erstellung der Zone das New-AzPrivateDnsRecordSet-Cmdlet, um Daten Satz Sätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-108">After the zone is created, use the New-AzPrivateDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="c3fb5-109">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-109">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c3fb5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3fb5-110">EXAMPLES</span></span>

### <span data-ttu-id="c3fb5-111">Beispiel 1: Erstellen einer privaten DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="c3fb5-111">Example 1: Create a Private DNS zone</span></span>
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

## <span data-ttu-id="c3fb5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3fb5-112">PARAMETERS</span></span>

### <span data-ttu-id="c3fb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3fb5-113">-DefaultProfile</span></span>
<span data-ttu-id="c3fb5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c3fb5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3fb5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c3fb5-115">-Name</span></span>
<span data-ttu-id="c3fb5-116">Gibt den Namen der privaten DNS-Zone an, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-116">Specifies the name of the private DNS zone to create.</span></span>

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

### <span data-ttu-id="c3fb5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3fb5-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3fb5-118">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-118">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="c3fb5-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3fb5-119">-Tag</span></span>
<span data-ttu-id="c3fb5-120">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-120">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="c3fb5-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3fb5-121">-Confirm</span></span>
<span data-ttu-id="c3fb5-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3fb5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3fb5-123">-WhatIf</span></span>
<span data-ttu-id="c3fb5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3fb5-125">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-125">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3fb5-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3fb5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3fb5-127">CommonParameters</span></span>
<span data-ttu-id="c3fb5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3fb5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3fb5-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3fb5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3fb5-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3fb5-130">INPUTS</span></span>

### <span data-ttu-id="c3fb5-131">Keine</span><span class="sxs-lookup"><span data-stu-id="c3fb5-131">None</span></span>

## <span data-ttu-id="c3fb5-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3fb5-132">OUTPUTS</span></span>

### <span data-ttu-id="c3fb5-133">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="c3fb5-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="c3fb5-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3fb5-134">NOTES</span></span>

## <span data-ttu-id="c3fb5-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3fb5-135">RELATED LINKS</span></span>

[<span data-ttu-id="c3fb5-136">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="c3fb5-136">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="c3fb5-137">Neu – AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3fb5-137">New-AzPrivateDnsRecordSet</span></span>](./New-AzPrivateDnsRecordSet.md)

[<span data-ttu-id="c3fb5-138">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="c3fb5-138">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)
