---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: d3e7a04f292be8e83bc28456c0510450c078a777
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850527"
---
# <span data-ttu-id="1a34f-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1a34f-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="1a34f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a34f-102">SYNOPSIS</span></span>
<span data-ttu-id="1a34f-103">Entfernt ein Speicherkonto aus Azure.</span><span class="sxs-lookup"><span data-stu-id="1a34f-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a34f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a34f-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a34f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a34f-105">DESCRIPTION</span></span>
<span data-ttu-id="1a34f-106">Das Cmdlet **Remove-AzureRmStorageAccount** entfernt ein Speicherkonto aus Azure.</span><span class="sxs-lookup"><span data-stu-id="1a34f-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="1a34f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a34f-107">EXAMPLES</span></span>

### <span data-ttu-id="1a34f-108">Beispiel 1: Entfernen eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1a34f-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="1a34f-109">Mit diesem Befehl wird das angegebene Speicherkonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="1a34f-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="1a34f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a34f-110">PARAMETERS</span></span>

### <span data-ttu-id="1a34f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a34f-111">-AsJob</span></span>
<span data-ttu-id="1a34f-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1a34f-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a34f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a34f-113">-DefaultProfile</span></span>
<span data-ttu-id="1a34f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a34f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a34f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1a34f-115">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a34f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1a34f-116">-Name</span></span>
<span data-ttu-id="1a34f-117">Gibt den Namen des zu entfernenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1a34f-117">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a34f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a34f-118">-ResourceGroupName</span></span>
<span data-ttu-id="1a34f-119">Gibt den Namen der Ressourcengruppe an, die das zu entfernende Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="1a34f-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a34f-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a34f-120">-Confirm</span></span>
<span data-ttu-id="1a34f-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a34f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a34f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a34f-122">-WhatIf</span></span>
<span data-ttu-id="1a34f-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a34f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a34f-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a34f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a34f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a34f-125">CommonParameters</span></span>
<span data-ttu-id="1a34f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a34f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a34f-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a34f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a34f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a34f-128">INPUTS</span></span>

### <span data-ttu-id="1a34f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1a34f-129">System.String</span></span>

## <span data-ttu-id="1a34f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a34f-130">OUTPUTS</span></span>

### <span data-ttu-id="1a34f-131">System. void</span><span class="sxs-lookup"><span data-stu-id="1a34f-131">System.Void</span></span>

## <span data-ttu-id="1a34f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a34f-132">NOTES</span></span>

## <span data-ttu-id="1a34f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a34f-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a34f-134">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1a34f-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="1a34f-135">Neu – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1a34f-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="1a34f-136">Satz-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1a34f-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


