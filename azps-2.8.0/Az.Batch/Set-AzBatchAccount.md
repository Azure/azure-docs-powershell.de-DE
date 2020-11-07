---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 0a19ede4a990b10244204d8f633ed747adb7d30e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847979"
---
# <span data-ttu-id="d3058-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d3058-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="d3058-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3058-102">SYNOPSIS</span></span>
<span data-ttu-id="d3058-103">Aktualisiert ein Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="d3058-103">Updates a Batch account.</span></span>

## <span data-ttu-id="d3058-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3058-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3058-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3058-105">DESCRIPTION</span></span>
<span data-ttu-id="d3058-106">Das Cmdlet " **Satz-AzBatchAccount** " aktualisiert ein Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="d3058-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="d3058-107">Derzeit kann dieses Cmdlet nur Tags aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d3058-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="d3058-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3058-108">EXAMPLES</span></span>

### <span data-ttu-id="d3058-109">Beispiel 1: Aktualisieren der Tags in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="d3058-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="d3058-110">Mit diesem Befehl werden die Tags für das Konto mit dem Namen pfuller aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d3058-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="d3058-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3058-111">PARAMETERS</span></span>

### <span data-ttu-id="d3058-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d3058-112">-AccountName</span></span>
<span data-ttu-id="d3058-113">Gibt den Namen des Batch Kontos an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d3058-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3058-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d3058-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="d3058-115">Gibt die Ressourcen-ID des speicherkontos an, das für den automatischen Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3058-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3058-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3058-116">-DefaultProfile</span></span>
<span data-ttu-id="d3058-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3058-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3058-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3058-118">-ResourceGroupName</span></span>
<span data-ttu-id="d3058-119">Gibt die Ressourcengruppe des Kontos an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="d3058-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3058-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="d3058-120">-Tag</span></span>
<span data-ttu-id="d3058-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="d3058-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d3058-122">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="d3058-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3058-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3058-123">CommonParameters</span></span>
<span data-ttu-id="d3058-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3058-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3058-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3058-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3058-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3058-126">INPUTS</span></span>

### <span data-ttu-id="d3058-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3058-127">System.String</span></span>

### <span data-ttu-id="d3058-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d3058-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d3058-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3058-129">OUTPUTS</span></span>

### <span data-ttu-id="d3058-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d3058-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d3058-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3058-131">NOTES</span></span>

## <span data-ttu-id="d3058-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3058-132">RELATED LINKS</span></span>

[<span data-ttu-id="d3058-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d3058-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="d3058-134">Neu – AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d3058-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="d3058-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="d3058-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="d3058-136">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="d3058-136">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
