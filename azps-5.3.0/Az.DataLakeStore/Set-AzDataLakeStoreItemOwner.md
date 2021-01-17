---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458033"
---
# <span data-ttu-id="9a679-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="9a679-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="9a679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a679-102">SYNOPSIS</span></span>
<span data-ttu-id="9a679-103">Ändert den Besitzer einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9a679-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9a679-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a679-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a679-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a679-105">DESCRIPTION</span></span>
<span data-ttu-id="9a679-106">Das **Cmdlet "Set-AzDataLakeStoreItemOwner"** ändert den Besitzer einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9a679-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9a679-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a679-107">EXAMPLES</span></span>

### <span data-ttu-id="9a679-108">Beispiel 1: Festlegen des Besitzers für ein Element</span><span class="sxs-lookup"><span data-stu-id="9a679-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="9a679-109">Mit diesem Befehl wird der Besitzer für das Stammverzeichnis auf "Desi Fuller" definiert.</span><span class="sxs-lookup"><span data-stu-id="9a679-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="9a679-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a679-110">PARAMETERS</span></span>

### <span data-ttu-id="9a679-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="9a679-111">-Account</span></span>
<span data-ttu-id="9a679-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9a679-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a679-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a679-113">-DefaultProfile</span></span>
<span data-ttu-id="9a679-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a679-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a679-115">-ID</span><span class="sxs-lookup"><span data-stu-id="9a679-115">-Id</span></span>
<span data-ttu-id="9a679-116">Gibt die Objekt-ID des AzureActive Directory-Benutzers, der Gruppe oder des Dienstprinzipal an, der bzw. der als Besitzer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a679-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a679-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a679-117">-PassThru</span></span>
<span data-ttu-id="9a679-118">Gibt an, dass der resultierende aktualisierte Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a679-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a679-119">-Path</span><span class="sxs-lookup"><span data-stu-id="9a679-119">-Path</span></span>
<span data-ttu-id="9a679-120">Gibt den Data Lake Store-Pfad des zu ändernden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="9a679-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a679-121">-Type</span><span class="sxs-lookup"><span data-stu-id="9a679-121">-Type</span></span>
<span data-ttu-id="9a679-122">Gibt den Typ des festgelegten Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="9a679-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="9a679-123">Die zulässigen Werte für diesen Parameter sind: Benutzer und Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9a679-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a679-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a679-124">-Confirm</span></span>
<span data-ttu-id="9a679-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a679-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a679-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9a679-126">-WhatIf</span></span>
<span data-ttu-id="9a679-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a679-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a679-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a679-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a679-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a679-129">CommonParameters</span></span>
<span data-ttu-id="9a679-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a679-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a679-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a679-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a679-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a679-132">INPUTS</span></span>

### <span data-ttu-id="9a679-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9a679-133">System.String</span></span>

### <span data-ttu-id="9a679-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9a679-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9a679-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="9a679-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="9a679-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9a679-136">System.Guid</span></span>

### <span data-ttu-id="9a679-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a679-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9a679-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a679-138">OUTPUTS</span></span>

### <span data-ttu-id="9a679-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9a679-139">System.String</span></span>

## <span data-ttu-id="9a679-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9a679-140">NOTES</span></span>

## <span data-ttu-id="9a679-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9a679-141">RELATED LINKS</span></span>

[<span data-ttu-id="9a679-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="9a679-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


